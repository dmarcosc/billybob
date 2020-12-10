<template>
  <div class="home">
    <div class="big-burger" >
      <img src="../assets/images/floatingburger.png" class="burger-home">
     </div>
    <div class="landing">
      <h1 class="landing-text">IT'S BURGER O'CLOCK</h1>
      <p class="greasy">warning! things may get
         <span style='color:red; cursor:pointer;'>greasy</span></p>
    </div>
  <div class="mid-landing">
    <h1 class="mid-landing-h1">American Diner & Bar</h1>
    <div class="mid-landing-div"><p class="left-mid-landing"></p>
    <p class="right-mid-landing"> ipsum wa orokanaru otouto yo,
       sole ni wa a ore ni kateru no wa ore dake da one does not simply walk into mordor
       have you heard any news from the other provinces ? nothing
        id like to talk abour my dear friend</p></div>
  </div>
  <div class="bottom-landing">
    <div style="padding:10em;">hola existo</div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'HomePage',
  components: {
  },
};
</script>

<style scoped>
.home{
  width:100%
}
.landing{
 height:90vh;
 /* background: rgb(245, 245, 65); */
 background: #F9C00E;
 text-align: center;
 font-weight: bold;
 font-family: "HWT Artz";
 padding:0 6em;
}
.landing-text{
  color:black;
  font-size:70px;
  /* margin-left:15em; */
  padding-top:6em;
  text-align: right;
}
.greasy{
  font-size:25px;
   text-align: right;
}
/******mid section**********/
.mid-landing{
  height:100%;
  background: white;
}
.mid-landing-h1{
margin:0;
font-size:60px;
padding-top:4em;
display:flex;
justify-content: center;
margin-left:10.6em;
}
.mid-landing-div{
 display: flex;

}
.left-mid-landing{
  width:54%;
}
.right-mid-landing{
  font-size:25px;
width:500px;
}
/******BOTTOM**********/
.bottom-landing{
   height:100%;
   background: red;
  color:white;
  display:flex;
}
/******BURGER********/
.burger-home{
  position: absolute;
  top:100px;
  z-index:1;
  height: 180vh;
}
</style>
