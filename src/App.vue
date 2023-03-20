<template>
  <h2>{{ text }}</h2>
  <Container>
    <ApartmentFilterForm 
    class="apartments-filter"
    @submit="logger"
    />
  </Container>
  
  <ApartmentsList :items="apartments ">
    
    <template v-slot:title>Selection according to choice</template>
<template v-slot:apartment="{apartment}">
  <ApartmentsItem
        :key="apartment.id"
        :descr="apartment.descr"
        :rating="apartment.rating"
        :imgSrc="apartment.imgUrl"
        :price="apartment.price"
        @click="handleItemClick"
      />
</template>

  </ApartmentsList>
</template>

<script>
import ApartmentsList from "./components/apartment/ApartmentsList.vue";
import ApartmentsItem from "./components/apartment/ApartmentsItem.vue";
import ApartmentFilterForm from './components/apartment/ApartmentFilterForm.vue';
import apartments from "./components/apartment/apartments";
import Container from './components/shared/Container.vue';

export default {
  name: "App",
  components: {
    ApartmentsList,
     ApartmentsItem,
     ApartmentFilterForm,
     Container,
  },
  data() {
    return {
      apartments,
      text: '',
    };
  },
  methods:{
    logger(value){
      console.log(value, '---form value')
    }
  }
};
</script>

<style lang="scss" scoped>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.apartments-filter{
  margin-bottom: 40px;
}

</style>
