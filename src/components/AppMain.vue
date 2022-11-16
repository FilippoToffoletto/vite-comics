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
      <div class="current">
        <div class="btn"><h4>current series</h4></div>
      </div>
      <div class="row">
        <ComicCard v-for="(item, index) in card" :key="index" :card="item"/>
      </div>
      <div class="btn"><h4>load more</h4></div>
    </div>
  </main>
</template>



<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;


main{
  background-color: #1C1C1C;
  color:white;
  font-size: 2.3rem;
  padding: 40px;
}
.row{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.btn{
  @include centerFlex('horizzontal');
  align-items: center;
  margin-top: 20px;
  h4{
    background-color: $Primary_Color;
    color:white;
    font-size: .9rem;
    width: calc(100% / 6);
    text-align: center;
    padding: 14px 0px;
    &:hover{
      cursor: pointer;
      background-color: white;
      color:$Primary_Color;
    }
  }
}
.container{
  position: relative;
  .current{
    position: absolute;
    top: -80px;
    left: -60px;
    @include centerFlex('horizzontal');
    align-items: center;
    h4{
      font-size: .9rem;
      width: 160px;
      text-align: center;
      padding: 14px 0px;
      
    }
  }
}

</style>