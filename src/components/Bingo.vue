<template>
    <div class="Container">
        <div class="Bingo">
        Bingo, vous avez un acheteur
        </div>
        <CenterLine />
    </div>
</template>

<script>
import CenterLine from './CenterLine'

export default {
  name: 'Bingo',
  components: {
    CenterLine,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Bingo {
    display: inline-block;
    background-color: black;
    color: white;
    line-height: 2em;
    padding: 0 15px;
    font-size: 1.3em;
}

.Container {
  position: relative;
  padding-bottom: 80px;
}
</style>
