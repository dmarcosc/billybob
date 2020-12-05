<template>
  <div id="app">
    <main>
    <HomePage />
    </main>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue';

export default {
  name: 'App',
  components: {
    HomePage,
  },
};
</script>

<style>
body {
  background:linear-gradient(to bottom, black , #020024);
  height:100%;
  background-attachment: fixed;
}
main {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  /* background:url('./assets/images/calleh.jpg'); */
  background:url('./assets/images/murocola.jpg'),url('./assets/images/pizzeria.jpg'),
  url('./assets/images/muroHojas.jpg');
  background-position:0px 0px, 600px 0px,1300px 0px;
  background-repeat: no-repeat;
  background-size: contain;
  min-height: 1000px;
  margin:0 auto;
}
</style>
