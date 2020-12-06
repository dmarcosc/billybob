<template>
  <div class="home">
    <nav class="nav-bar">
      <label class="nav-bar-label">LOCATION</label>
      <label class="nav-bar-label">FOOD</label>
      <div class="nav-div-logo">
      <img src="../assets/images/logo2.jpg" class="logo">
      </div>
      <label class="nav-bar-label">ABOUT</label>
      <label class="nav-bar-label">CONTACT</label>
      <div class="div-social-icons">
        <img src="../assets/images/ig.svg" class="nav-bar-icon">
        <img src="../assets/images/fb.png" class="nav-bar-icon">
      </div>
    </nav>
    <hr>
    <div class="img-body-entrance">
      <img src="../assets/images/calleh.jpg" style="height:450px;">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {

  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  height:900px;
}

/*****NAV-BAR*****/
.logo{
  border-radius: 110px;
  width:170px;
  margin: 0 10px;
}
.nav-bar{
display:flex;
align-items: center;
justify-content: center;
height:170px;
padding:10px;
color:wheat;
font-weight: 600;
font-size:26px;
}
.nav-bar-label{
margin: 15px;
}
.nav-bar-icon{
  margin: 0 5px;
  width:40px;
}
.div-social-icons{
  width: 100%;
  margin-right: 3em;
  text-align: right;
  position: absolute;
}

/******body********/
.img-body-entrance{
display: flex;
justify-content: center;
}
</style>
