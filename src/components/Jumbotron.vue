<script>
export default {
    name:'Jumbotron'
}
</script>

<template>
  <div class="container-fluid">
    <img src="../assets/img/jumbotron.jpg" alt="">
  </div>
</template>



<style lang="scss" scoped>
.container-fluid{
    height: 400px;
    width: 100vw;
    background-color: blue;
    overflow: hidden;
    img{
        object-fit: contain;
    }
}


</style>