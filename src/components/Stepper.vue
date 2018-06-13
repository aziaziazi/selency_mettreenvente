<template>
  <div>
    <Step v-bind="stepsContent.identification" />
    <Step v-bind="stepsContent.boutique" />
    <Step v-bind="stepsContent.validation" />
    <Bingo />
    <Step v-bind="stepsContent.livraison" />
    <Step v-bind="stepsContent.virement" />
  </div>
</template>

<script>
import Bingo from "./Bingo"
import Step from "./Step"
import identification from  "../assets/identification.svg"
import boutique from  "../assets/boutique.svg"
import validation from  "../assets/validation.svg"
import livraison from  "../assets/livraison.svg"
import virement from  "../assets/virement.svg"

export default {
  name: 'Stepper',
  components: {
    Step,
    Bingo,
  },
  props: {
    msg: String
  },
  data: function() {
    return {
      stepsContent: {
        identification: {
          stepTitle: "Identifiez-vous",
          stepText: "en créant votre compte en quelques clics",
          stepNumber: 1,
          imageSource: identification,
        },
        boutique: {
          stepTitle: "Créez votre boutique",
          stepText: "et ajoutez des articles via notre formulaire de mise en ligne",
          stepNumber: 2,
          imageSource: boutique,
        },
        validation: {
          stepTitle: "Nous sélectionnons",
          stepText: "et validons (sous 24H minimum) la mise en vente de vos articles",
          stepNumber: 3,
          imageSource: validation,
          textOnRight: true,
        },
        livraison: {
          stepTitle: "Organisez la livraison",
          stepText: "de vos articles (sachez que nous avons un service de transport qui peut s'occuper de les livrer pour vous)",
          stepNumber: 4,
          imageSource: livraison,
        },
        virement: {
          stepTitle: "Nous vous payons",
          stepText: "par virement bancaire",
          stepNumber: 5,
          textOnRight: true,
          imageSource: virement,
        },
      },
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
