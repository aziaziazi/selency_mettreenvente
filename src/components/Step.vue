<template>
    <div
      class="stepContainer"
      v-bind:class="{textOnRight}"
    >
      <div class="textContainer">
        <h2>{{stepTitle}}</h2>
        <p>{{stepText}}</p>
      </div>
      <div class="stepNumber">{{stepNumber}}</div>
      <div class="imageContainer">
        <!-- toodo: add label -->
        <img src="../assets/logo.png">
      </div>
      <div class="centerLine"/>
    </div>
</template>

<script>
export default {
  name: 'Step',
  props: {
    stepNumber: {
      type: String,
      required: true
    },
    stepText: {
      type: String,
      required: true
    },
    stepTitle: {
      type: String,
      required: true
    },
    textOnRight: {
      type: Boolean,
      required: false,
      default: false,
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  p {
    font-family: Arial, Helvetica, sans-serif;
    margin-top: 0;
  }

  h2 {
    margin: 0 0 0.2em;
  }

  .centerLine {
    position: absolute;
    left: calc(50% - 1px);
    height: 100%;
    width: 0;
    border-left: 2px solid black;
    z-index: -1;
  }

 .stepContainer {
   display: flex;
   justify-content: center;
   align-items: flex-start;
   position: relative;
 }

.textContainer, .imageContainer {
  flex: 1 1 50%;
  max-width: 500px;
}

.textContainer {
  text-align: right;
  order: 1;
}

.imageContainer {
  float: left;
  order: 3;
}

.textOnRight > .textContainer {
  text-align: left;
  order: 3;
}

.textOnRight > .imageContainer {
  order: 1;
}

.stepNumber {
  flex: none;
  color: white;
  background-color: black;
  font-size: 1.5em;
  width: 40px;
  line-height: 40px;
  border-radius: 20px;
  text-align: center;
  vertical-align: middle;
  order: 2;
  margin: 0 40px;
}

</style>
