<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import DcBar from './components/DcBar.vue';
import AppFooter from './components/AppFooter.vue';
import FindUsBar from './components/FindUsBar.vue';
import Jumbotron from './components/Jumbotron.vue';

export default {
  name: 'App',
  components:{
    AppHeader,
    AppMain,
    DcBar,
    AppFooter,
    FindUsBar,
    Jumbotron
  }
}
</script>

<template>
  <AppHeader />
  <Jumbotron />
  <AppMain />
  <DcBar />
  <AppFooter />
  <FindUsBar />
</template>



<style lang="scss">
@use './style/general.scss'; 

</style>