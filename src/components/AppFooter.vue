<script>
export default {
    name:'AppFooter'
}
</script>

<template>
  <footer>
    <div class="container">
      <!-- DC COMICS -->
      <div class="col">
        <nav>
          <h4>dc comics</h4>
          <ul>
            <li><a href="#">Characters</a></li>
            <li><a href="#">comics</a></li>
            <li><a href="#">movies</a></li>
            <li><a href="#">tv</a></li>
            <li><a href="#">games</a></li>
            <li><a href="#">videos</a></li>
            <li><a href="#">news</a></li>
          </ul>
        </nav>
        <!-- /DC COMICS -->
      
        <!-- SHOP -->
        <nav>
          <h4>shop</h4>
          <ul>
            <li><a href="#">shop DC</a></li>
            <li><a href="#">shop DC collectibles</a></li>
          </ul>
        </nav>
      </div>
      <!-- /SHOP -->

      <!-- DC -->
      <div class="col">
        <nav>
          <h4>dc</h4>
          <ul>
            <li><a href="#">Term of use</a></li>
            <li><a href="#">privacy policy (new)</a></li>
            <li><a href="#">ad choices</a></li>
            <li><a href="#">advertising</a></li>
            <li><a href="#">jobs</a></li>
            <li><a href="#">subscriptions</a></li>
            <li><a href="#">talent workshops</a></li>
            <li><a href="#">CPSC cerrtificates</a></li>
            <li><a href="#">ratings</a></li>
            <li><a href="#">Shop help</a></li>
            <li><a href="#">contact us</a></li>
          </ul>
        </nav>
      </div>
      <!-- /DC -->
      <!-- SITES -->
      <div class="col">
        <nav>
          <h4>sites</h4>
          <ul>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </nav>
      </div>
      <!-- /SITES -->
    </div>
    <div class="layer">
      <img src="../assets/img/dc-logo-bg.png" alt="DC comics">
    </div>
  </footer>
</template>



<style lang="scss" scoped> 
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;


footer{
  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  overflow: hidden;
  padding: 30px 0px;
  position: relative;
}
h4{
  color: white;
  font-size: 1.2rem;
  padding-bottom: 10px
}

.container{
  @include centerFlex('vertical');
  align-items: flex-start;
  ul{
    padding-bottom: 10px;
    margin-right: 20px;
    li{
      margin: 2px 0px;
      a{
        text-transform: capitalize;
        color: #7F7F7F;
        font-size: .8rem;
        &:hover{
          color: white;
          text-decoration: underline;
        }
      }
    }
  }
}
.layer{
  position: absolute;
  bottom: -50px;
  right: 250px;
  img{
    width: 95%;
  }
}


</style>