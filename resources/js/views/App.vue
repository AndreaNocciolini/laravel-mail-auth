<template>
  <div class="container">
      <Header></Header>
      <router-view></router-view>
      <!-- <Main></Main> -->
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import Main from '../components/Main.vue';

export default {
    name: 'App',
    components: {
        Header,
        Main
    }
}
</script>

<style>

</style>