<template>
  <!-- <div class="grid-view   " v-on:scroll="onScroll">-->
  <div class="grid-view  " v-on:scroll="onScroll">
    <div class="grid-data">
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
      <grid-cell></grid-cell>
    </div>
  </div>
</template>

<script>
  import GridCell from "./grid-cell";

  export default {
    name: "grid-content",
    components: {GridCell},
    methods: {
      onScroll: function (e) {
        this.$emit('onScroll', {x: this.$el.scrollLeft, y: this.$el.scrollTop});
      }
    }
  }
</script>

<style scoped>
  .grid-view {
    width: 30em;
    height: 15em;
    position: absolute;
    left: 6em;
    top: 3em;
    overflow: auto;
  }

  .grid-data {
    position: relative;
    z-index: 5;
    width: 60em;
    height: 30em;
  }
</style>
