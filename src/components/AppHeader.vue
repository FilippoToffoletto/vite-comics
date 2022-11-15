<script>
export default {
    name:'AppHeader'
}
</script>

<template>
  <header class="container">
    <div class="logo">
      <img src="/dc-logo.png" alt="Logo DC-comics">
    </div>
    <nav>
      <ul>
        <li><a href="#">CHARACTERS</a></li>
        <li><a href="#">COMICS</a></li>
        <li><a href="#">MOVIES</a></li>
        <li><a href="#">TV</a></li>
        <li><a href="#">GAMES</a></li>
        <li><a href="#">COLLECTIBLES</a></li>
        <li><a href="#">VIDEOS</a></li>
        <li><a href="#">FANS</a></li>
        <li><a href="#">NEWS</a></li>
        <li><a href="#">SHOP</a></li>
      </ul>
    </nav>
  </header>
</template>



<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

header{
  height: 120px;
  display: flex;
  justify-content: space-between;
  @include centerFlex('vertical');
  .logo{
    margin-right: 100px;
    width: 100px;
    img{
      width: 80px;
    }
  }
  ul{
    display: flex;
    li{
      padding: 47px 10px;
      &:hover{
        border-bottom: 5px solid $Primary_Color;
      }
      a{
          text-transform: uppercase;
          font-weight: 600;
          font-size: 0.9rem;
        }
    }
  }
}

</style>