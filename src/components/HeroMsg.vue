<template>
  <div class="hero-msg">
    <h2>{{ myName }}</h2>
    <h1>{{ occupation }}</h1>
    <p>{{ heroMessage }}</p>
    <Button btnText="VIEW WORKS" btnUrl="#"/>
    <Button btnText="CONTACT ME" btnUrl="#"/>
  </div>
</template>

<script>
import Button from "./Button.vue"

export default {
  data() {
    return {
      myName: "Zalim Tsorionov",
      occupation: "Web Developer",
      heroMessage: "I am Zalim, a dedicated multidisciplinary designer who pays special attention to the details. My goal is to create both: visually appealing and practical design."
    }
  },
  components: {
    Button
  }
}
</script>

<style>

</style>