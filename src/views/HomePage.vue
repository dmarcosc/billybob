<template>
  <div class="home">
    <div class="big-burger" >
      <img src="../assets/images/floatingburger.png" class="burger-home">
     </div>
    <div class="landing">
      <div class="top-container">
        <h1 class="landing-text">IT'S BURGER O'CLOCK</h1>
        <p class="greasy">warning! things may get
          <span style='color:red; cursor:pointer;'>greasy</span>
        </p>
      </div>
    </div>
  <div class="mid-landing">
    <div class="mid-container">
      <h1 class="mid-landing-h1">
        American Diner & Bar
      </h1>
      <p class="mid-landing-p"> ipsum wa orokanaru otouto yo,
        sole ni wa a ore ni kateru no wa ore dake da one does not simply walk into mordor
        have you heard any news from the other provinces ? nothing
        id like to talk abour my dear friend
      </p>
    </div>
  </div>
  <div class="bottom-landing">
    <div class="bot-container">hola existo</div>
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
  width:100%;
}
/**TOP CONTAINER */
.landing{
 height:80vh;
 background: #F9C00E;
 text-align: right;
 display:flex;
 justify-content: flex-end;
 align-items: center;
 font-weight: bold;
 font-family: "HWT Artz";
 /* padding-right:4em; */
 margin-top:100px;
}
.top-container{
  padding-right: 4em;
}
.landing-text{
  color:black;
  font-size:70px;
}
.greasy{
  font-size:25px;
}

/******mid section**********/
.mid-landing{
  height:80vh;
  width:100%;
  background: white;
  display:flex;
  justify-content: flex-end;
  align-items: center;
}
.mid-container{
  flex:0.5;
}
.mid-landing-h1{
font-size:60px;
}
.mid-landing-p{
  font-size:25px;
}
/******BOTTOM**********/
.bottom-landing{
   height:60vh;
  width:100%;
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
