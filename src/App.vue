<template>
 
 <!-- <HomeButton  @:click="increment">Click me</HomeButton> -->
<!-- <ApartmentsItem 
:descr="apartment.descr" 
:price="apartment.price" 
:rating="apartment.rating" 
/> -->
<ApartmentsList :items="apartments"/>
</template>

<script>

// import HomeButton from "./components/HomeButton.vue"
// import ApartmentsItem from "./components/apartment/ApartmenstItem.vue"
import ApartmentsList from './components/apartment/ApartmentsList.vue';
import apartments from "./components/apartment/apartments"

export default {
  name: 'App',
  components: {
    // HomeButton,
    // ApartmentsItem,
    ApartmentsList,
  },
  data(){
    return {
      apartments,
      apartment:{
        id: '5fjiiojfgj4jj4gp4ugj45g9',
        title: "Apartment",
        descr: "Luxurious Scandinavian-style apartment with panoramic river views and free Wi-Fi.",
        price:2032,
        rating: 3.5,
location: {
  city: "Sydney"
}, owner:{
  name: "Eilen",
  phone: '115-355-5652',
  email: 'Eilen@gmail.com'
}
      }
    }
  }
  // data() {
  //   return {
  //     amountOfClicks: 0,
  //   }
  // },
  // computed: {
  //   title() {
  //     return `Amount of clicks ${this.amountOfClicks}`
  //   }
  // },
  // methods: {
  //   increment() {
  //     this.amountOfClicks += 1
  //   }
  // }
}
</script>

<style>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
