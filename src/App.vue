<template>
  <HeaderMain />
 

</template>

<script>
import HeaderMain from "./components/Header"


export default {
  name: 'App',
  components: {
    HeaderMain,
  },
  data(){
    return {
      
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  /* width: 100%; */
  max-width: 1366px;
  margin: auto;
  padding: 0 40px;
}

.d-f {
  display: flex;
}

.d-fc {
  display: flex;
  align-items: center;
  justify-content: center;
}

.d-fsb {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
