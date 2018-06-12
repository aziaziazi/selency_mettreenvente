<template>
  <h1>
    {{title}}
  </h1>
</template>

<script>
export default {
  name: 'Title',
  data() {
    return {
      title: 'Comment ça marche ?',
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    font-size: 3rem;
    letter-spacing: 0.1rem;
    margin-bottom: 100px;
  }
</style>
