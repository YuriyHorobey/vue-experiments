<template>
  <div class="ruler   ruler-view"
       v-bind:class="{ 'ruler-horizontal': type=='horizontal', 'ruler-vertical': type=='vertical'}">
    <div class="ruler-cells">
      <div class="cell">0</div>
      <div class="cell">1</div>
      <div class="cell">2</div>
      <div class="cell">3</div>
      <div class="cell">4</div>
      <div class="cell">5</div>
      <div class="cell">6</div>
      <div class="cell">7</div>
      <div class="cell">8</div>
      <div class="cell">9</div>
      <div class="cell hack-cell"><!--scrollbar size hack--></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "grid-ruler",
    props: {type: String, scroll: Number},
    watch: {
      scroll: function ( newPosition,oldPosition ) {
        /**
         * I'm trying my best to make scrolling smooth..
         */
        // this.$nextTick(function() {
        //   this.type == 'horizontal'
        //     ? this.$el.scrollTo(newPosition, 0)
        //     : this.$el.scrollTo(0, newPosition)
        // });

      }
    }

  }
</script>

<style scoped>
  /*
 Rules for both H&V rulers
  */
  .ruler {
    position: absolute;
    overflow: hidden;
  }

  .ruler-cells {

  }

  .ruler .cell {
    background-color: #efefef;
    padding-top: 1em;
  }

  .hack-cell {
    border: none;
  }

  /*Horizontal Ruler*/
  .ruler-horizontal.ruler-view {
    width: 30em;
    left: 6em; /*cell width*/
    top: 0;
    height: 3em;

  }

  .ruler-horizontal.ruler-view .ruler-cells {
    width: 66em; /*more than it has cells to fix scrollbar width issue*/
  }

  /*Vertical Ruler*/
  .ruler-vertical.ruler-view {
    width: 6em; /*cell width*/
    left: 0;
    top: 3em;
    height: 15em;

  }

  .ruler-vertical.ruler-view .ruler-cells {
  }
</style>
