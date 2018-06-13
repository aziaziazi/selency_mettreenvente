<template>
    <div class="centerLine"/>
</template>

<script>
export default {
  name: 'CenterLine',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .centerLine {
    position: absolute;
    left: calc(50% - 1px);
    height: 100%;
    width: 0;
    border-left: 2px solid black;
    z-index: -1;
  }
</style>
