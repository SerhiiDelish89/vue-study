<template>
  <h1>{{ title }}</h1>
 <HomeButton  @:click="increment">Click me</HomeButton>
<StarRating :rating="4"/>


</template>

<script>

import HomeButton from "./components/HomeButton.vue"
import StarRating from "./components/StartRating.vue"


export default {
  name: 'App',
  components: {
    HomeButton,
    StarRating,
  },
  data() {
    return {
      amountOfClicks: 0,
    }
  },
  computed: {
    title() {
      return `Amount of clicks ${this.amountOfClicks}`
    }
  },
  methods: {
    increment() {
      this.amountOfClicks += 1
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
</style>
