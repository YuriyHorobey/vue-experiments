<template>
  <div class=" unlimited-grid-container">
    <data-loader :loading=loading></data-loader>
    <grid-ruler type="horizontal" :scroll=scrollX></grid-ruler>
    <grid-ruler type="vertical" :scroll=scrollY></grid-ruler>
    <grid-content @onScroll="gridHasScrolled"></grid-content>
  </div>

</template>

<script>
  import DataLoader from "./data-loader";
  import GridRuler from "./grid-ruler";
  import GridContent from "./grid-content";

  export default {
    name: "UnlimitedGrid",
    components: {GridContent, GridRuler, DataLoader},

    data: () => {
      return {
        loading: true,
        scrollX: 0,
        scrollY: 0
      }
    },
    methods: {
      gridHasScrolled: function (position) {
        this.$data.scrollX = position.x;
        this.$data.scrollY = position.y;
      }
    },

    mounted: function () {
      /*
      Finally after lots of tries with $emit/$watch
between child-parent-child components, I ended up with this ugly
but working solution.
$emit/$watch is slow. There is clearly visible difference in moving between
grid and ruler(((
Probably Vue has some means for animation as Angular has, but since this is
a Test project and I'm in the process of migration from Angular to Vue
I definitely have no time to master Vue animation techniques.

Sad but true.
       */
      var gridContainer = this.$el;
      var rullerXView = gridContainer.querySelector(".ruler.ruler-horizontal.ruler-view");
      var rullerYView = gridContainer.querySelector(".ruler.ruler-vertical.ruler-view");
      var gridView = gridContainer.querySelector(".grid-view");

      gridView.addEventListener('scroll', function (e) {
        rullerXView.scrollTo(gridView.scrollLeft, 0);
        rullerYView.scrollTo(0, gridView.scrollTop);
      })
    }


  }
</script>

<style scoped>
  .unlimited-grid-container {
    width: 36em;
    height: 18em;
    position: relative;
    overflow: hidden;
  }
</style>
