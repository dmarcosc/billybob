<template>
  <div class="home">
    <div class="big-burger" >
      <img src="../assets/images/floatingburger.png" class="burger-home">
     </div>
    <div class="landing">
      <div class="landing-text">
      IT'S BURGER O'CLOCK
     </div>
    </div>
  <div class="mid-landing">
  </div>
  <div class="bottom-landing">
    <div class="bottom-landing-div">
      <div class="bottom-landing-cards">
        <p class="titles-bottom-cards">OPENING HOURS</p>
        <br>
        <p>SUND-THU______________20:00-00:00</p>
        <p>FRI-SAT________________20:00-00:30</p>
      </div>
      <div class="bottom-landing-cards">
        <p class="titles-bottom-cards">LOCATIONS</p>
        <br>
        <p>Calle Fray Ceferino, 11, 33001 Oviedo, Asturias</p>
        <p>Calle Magdalena, 20, 33009 Oviedo, Asturias</p>
      </div>
      <div class="bottom-landing-cards">
        <p class="titles-bottom-cards">CONTACT</p>
        <br>
        <p>984 49 63 02 <i class="fas fa-phone-alt"></i></p>
        <p>billyboboviedo@gmail.com <i class="fas fa-envelope solid"></i></p>
      </div>
    </div>
    <div class=bottom-logo></div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'HomePage',
};
</script>

<style scoped>
.home{
  height:100%;
  width:100%
}
.landing{
 height:90vh;
 /* background: rgb(245, 245, 65); */
 background: #F9C00E;
 display:flex;
 justify-content: center;
 align-items: center;
 font-weight: bold;
}
.landing-text{
  color:black;
  font-size:44px;
  margin-left:500px;
   border: 2px solid black;
}
.mid-landing{
  height:80vh;
  background: white;

}
/******BOTTOM**********/
.bottom-landing{
  height:270px;
  background: black;
  color:white;
  border-top:3px solid black;
  display:flex;
  justify-content: flex-end;

}
.bottom-landing-div{
  padding-top:5em;
  display:flex;
}
.bottom-landing-cards{
  font-size: 12px;
  margin-right:40px;
}
.titles-bottom-cards{
  font-size:14px;
  font-weight: bold;
}
.bottom-logo{
  margin-top:60px;
  margin-right:20px;
  padding:0;
  width:170px;
  height:170px;
  background-size: 120% !important;
 background-position: center !important;
  background: url('~@/assets/images/logo3.jpg') no-repeat;
  border-radius: 110px;
}
@media  screen and (max-width:1520px) {
  .bottom-landing-cards{
  font-size:10px;
  }
  .titles-bottom-cards{
    font-size:12px;
  }
  .bottom-landing-cards{
    margin-right:20px;;
  }
  .bottom-logo{
    width:120px;
  }
}
/******BURGER********/
.burger-home{
  position: absolute;
  top:100px;
  z-index:1;
  height: 180vh;
}
.big-burger{
}
</style>
