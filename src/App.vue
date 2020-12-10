<template>
  <div id="app">
    <main>
    <NavBar />
    <HomePage />
    <Footer style="z-index:6;" />
    </main>
  </div>
</template>

<script lang="js">
import HomePage from './views/HomePage.vue';
import NavBar from './components/NavBar.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    HomePage,
    NavBar,
    Footer,
  },
};
</script>

<style>
body {
  background:black;
  height: 100%;
  width: 100%;
  display:flex;
  position:absolute;
  /* background-attachment: fixed; */
  margin: 0;
}
main {
  font-family: "HWT Artz", Helvetica, Arial, sans-serif;
  width: 100%;
  position:absolute;
  /* background:url('./assets/images/calleh.jpg'); */
  /* background:url('./assets/images/murocola.jpg'),url('./assets/images/pizzeria.jpg'),
  url('./assets/images/muroHojas.jpg');
  background-position:0px 0px, 600px 0px,1300px 0px; */
  /* background:url('./assets/images/tablones5.jpg'); */
  /* background-repeat: no-repeat; */
  background-size: contain;
  margin:0 auto;
  height: 100%;
}
</style>
