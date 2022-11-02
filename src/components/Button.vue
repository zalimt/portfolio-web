<template>
    <a :href="btnUrl">{{ btnText }}</a>
</template>

<script>
export default {
  name: "ButtonComp",
  props: [ "btnText", "btnUrl" ],
}
</script>

<style>

</style>