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
        <img v-bind:src="imageSource">
      </div>
      <CenterLine />
    </div>
</template>

<script>
import CenterLine from './CenterLine'

export default {
  name: 'Step',
  components: {
    CenterLine,
  },
  props: {
    stepNumber: {
      type: Number,
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
    },
    imageSource: {
      type: String,
      required: false,
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

 .stepContainer {
   display: flex;
   justify-content: center;
   align-items: flex-start;
   position: relative;
   padding-bottom: 50px;
 }

.textContainer, .imageContainer {
  flex: 1 1 50%;
  max-width: 280px;
}

.textContainer {
  text-align: right;
  order: 1;
}

.imageContainer {
  order: 3;
}

.imageContainer > img {
  float: left;
  width: 65px;
}

.textOnRight > .textContainer {
  text-align: left;
  order: 3;
}

.textOnRight > .imageContainer {
  order: 1;
}

.textOnRight > .imageContainer > img {
  float: right;
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
  margin: 0 30px;
}

</style>
