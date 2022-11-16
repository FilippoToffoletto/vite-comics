<script>
import ComicCard from './ComicCard.vue';
import card from '../data/cards';
export default {
    name:'AppMain',
    components:{
      ComicCard
    },
    data(){
        return{
            card
        }
    }
}
</script>

<template>
  <main>
    <div class="container">
      <p>--->Content goes here </p>
      <ComicCard v-for="(item, index) in card" :key="index" :card="item"/>
    </div>
  </main>
</template>



<style lang="scss" scoped>
@use '../style/partials/variables' as *;

main{
  background-color: #1C1C1C;
  color:white;
  font-size: 2.3rem;
  padding: 40px;
}

</style>