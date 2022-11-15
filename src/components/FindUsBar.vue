<script>
export default {
    name:'FindUsBar',
    data(){
      return{
        socials:[
          {
            urlImage:'footer-facebook.png',
            text:'Facebook',
            current:false
          },
          {
            urlImage:'footer-twitter.png',
            text:'twitter',
            current:false
          },
          {
            urlImage:'footer-youtube.png',
            text:'youTube',
            current:false
          },
          {
            urlImage:'footer-pinterest.png',
            text:'pinterest',
            current:false
          },
          {
            urlImage:'footer-periscope.png',
            text:'periscope',
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
  <section>
    <div class="container">
    <div class="left">
      <div class="btn"><h3>sing-up now</h3></div>
    </div>
    <div class="right">
      <h3>follow us</h3>

      <ul>
        <li
        v-for="(link, index) in socials"
        :key="index"
        >
          <div class="img">
            <img :src="getImagePath(link.urlImage)" alt="link.text">
          </div>
        </li>
      </ul>

    </div>
  </div>
  </section>
</template>



<style lang="scss" scoped> 
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;


section{
  background-color:#303030;
  height: 100%;
}
.container{
  @include centerFlex('horizzontal');
  justify-content: space-between;
  padding: 20px 0px;
  h3{
    font-size: 1.4rem
  }
  .left{
    .btn{
      border: 1px solid $Primary_Color;
      padding: 10px;
      h3{
        color: white;
      }
    }
  }
  .right{
    padding: 10px;
    @include centerFlex('vertical');
    justify-content: space-between;
    h3{
      color:$Primary_Color;
      padding: 0px 20px;
    }
    ul{
      @include centerFlex('vertical');
      justify-content: space-between;
      li{
        padding: 0px 10px;
      }
    }
  }
  
}

</style>