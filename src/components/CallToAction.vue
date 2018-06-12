<template>
  <div class="container">
    <h2>
      {{calltoActionTitle}}
    </h2>
    <button>
      {{calltoActionLabel}}
    </button>
  </div>
</template>

<script>
export default {
  name: 'CallToAction',
  data() {
    return {
      calltoActionTitle: "C'est parti ?",
      calltoActionLabel: "Vendez",
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  font-size: 1.5em;
  margin-bottom: 5px;
}
button {
  border: none;
  /* todo: use constant */
  background: black;
  color: white;
  padding: 13px 35px;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1.2em;
  text-transform: uppercase;
}

.container {
  margin-top: 100px;
}
</style>
