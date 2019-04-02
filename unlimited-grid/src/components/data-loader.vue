<template>
  <div class="cell data-loading-cell" v-if="loading"><img src="../assets/loading9.gif"></div>
</template>

<script>
  export default {
    name: "data-loader",
    props: {loading: Boolean}
  }
</script>

<style scoped>
  .data-loading-cell {
    position: absolute;
    top: 0;
    left: 0;
    text-align: center;
    padding-top: 8px;
  }
</style>
