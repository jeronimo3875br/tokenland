<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
  import { Component, Vue } from 'vue-property-decorator';
  import Header from './components/header';

  @Component({
    components: {
      Header,
    },
  })

  export default class App extends Vue {}
</script>

<style scoped>
#app {
  height: 100vh;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 10% 90%;
}
</style>