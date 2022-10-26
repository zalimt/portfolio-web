<template>
  <HeaderMain />
  <Carousel>
    <Slide v-for="(slide, index) in works" :key="index">

    </Slide>
  </Carousel>
 

</template>

<script>
import HeaderMain from "./components/Header"
import Carousel from "./components/Carousel"
import Slide from "./components/Slide"


export default {
  name: 'App',
  components: {
    HeaderMain,
    Carousel,
    Slide
  },
  setup() {
    const works = ["ws-1", "ws-2", "ws-3", "ws-4", "ws-5", "ws-6", "ws-7", "ws-8"];

    return works
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
  padding-top: 40px;
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
