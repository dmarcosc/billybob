<template>
  <div class="home">
    <NavBar></NavBar>
    <hr>
    <div class="img-body-entrance">
      <img src="../assets/images/calleh.jpg" style="height:450px;">
    </div>
    <div class="img-body-entrance">
      <img src="../assets/images/callebalcon.jpg" style="height:450px;">
    </div>
    <div class="img-body-entrance">
      <img src="../assets/images/calleh.jpg" style="height:450px;">
    </div>
  </div>
</template>

<script>
import NavBar from '../components/NavBar.vue';

export default {
  name: 'HomePage',
  components: {
    NavBar,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  height:900px;
}
/******body********/
.img-body-entrance{
display: flex;
justify-content: center;
}
</style>
