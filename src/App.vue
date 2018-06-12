<template>
  <div id="app">
    <Title />
    <Stepper />
    <CallToAction />
  </div>
</template>

<script>
import Title from './components/Title'
import Stepper from './components/Stepper'
import CallToAction from './components/CallToAction'
// load 'Caslon Graphique EFa' in free version until 12/07/2018
(function() {
    var trial = document.createElement('script');
    trial.type = 'text/javascript';
    trial.async = true;
    trial.src = 'https://easy.myfonts.net/v2/js?sid=63669(font-family=Caslon+Graphique+EF)&key=kUtVku8wWh';
    var head = document.getElementsByTagName("head")[0];
    head.appendChild(trial);
})();

export default {
  name: 'app',
  components: {
    Title,
    Stepper,
    CallToAction,
  }
}
</script>

<style>

#app {
  font-family: 'Caslon Graphique EF', Baskerville, Times;
  text-align: center;
  margin-top: 60px;
}
</style>
