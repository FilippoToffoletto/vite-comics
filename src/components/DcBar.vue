<script>
export default {
    name:'DcBar',
    data(){
      return{
        navContent: [
          {
            urlImg:'buy-comics-digital-comics.png',
            text:'Digital Comics',
            current:false
          },
          {
            urlImg:'buy-comics-merchandise.png',
            text:'DC merchandise',
            current:false
          },
          {
            urlImg:'buy-comics-subscriptions.png',
            text:'subscrition',
            current:false
          },
          {
            urlImg:'buy-comics-shop-locator.png',
            text:'comic shop locator',
            current:false
          },
          {
            urlImg:'buy-dc-power-visa.svg',
            text:'Dc power visa',
            current:false
          },
        ]
      }
    },
    methods:{
      getImagePath(imageName){
        return new URL(`../assets/img/${imageName}`, import.meta.url).href
      }
    }
}
</script>

<template>
  <nav>
    <div class="container">
      <ul>
        <li
        v-for="(link, index) in navContent"
        :key="index"
        >
          <div class="img">
            <img :src="getImagePath(link.urlImg)" alt="link.text">
          </div>
          <a href="#">{{link.text}}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>



<style lang="scss" scoped> 
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

nav{
  background-color: $Primary_Color;
  color: white;
  padding: 20px 0px;
}
ul{
  @include centerFlex ('horizzontal');
  justify-content: space-around;
  li{
    @include centerFlex;
    width: calc(100% / 5);
    text-transform: uppercase;
    .img{
      width: 50%;
      img{
        transform: scale(.5);
      }
    }
    a{
      color: white;
      font-size: .9rem;
    }
  }
}

</style>