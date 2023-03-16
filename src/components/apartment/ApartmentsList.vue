<template>
    <HomeContainer>
    <div class="apartments-list">
<ApartmentsItem v-for="{id, descr, rating, imgUrl, price} in items" 
:key="id" 
:descr="descr"
 :rating="rating"
:imgSrc="imgUrl"
:price="price"
/>
    </div>
</HomeContainer>
</template>



<script>

import ApartmentsItem from './ApartmentsItem.vue'
import HomeContainer from "../shared/Container.vue"
    export default {
        name: "ApartmentsList",
        components:{
            ApartmentsItem,
            HomeContainer,
        },
        props: {
            items:{
                type: Array,
                default: ()=>[],
            }
        }
    }
</script>

<style lang="scss" scoped>
.apartments-list {
  display: inline-flex;
  flex-wrap: wrap;
  margin-left: -15px;
  margin-right: -15px;
}
</style>