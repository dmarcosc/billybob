<template>
  <nav class="nav-bar">
    <button @click="changeLogo=!changeLogo"
              :class="{ 'home-button':changeLogo , 'home-button american': !changeLogo }">
      </button>
      <ul class="nav-bar-left">
        <li :class="{'nav-bar-li open':isOpen ,'nav-bar-li close': !isOpen }">
          <span v-if='isOpen'>
            OPEN <br> NOW !
          </span>
          <span v-if='!isOpen'>
            CLOSED <p style="font-size:9px;">We'll be back in {{time}}</p>
          </span>
        </li>
        <li class="nav-bar-li">
          <span>
            OUR <br> CHALLENGE
          </span>
          <span>
            <i class="fas fa-trophy"></i>
          </span>
        </li>
        <li class="nav-bar-li">
          <span>
            FOOD <br> & DRINK
          </span>
          <span>
            <i class="fas fa-utensils"></i>
          </span>
        </li>
      </ul>
      <ul class="nav-bar-right">
        <li class="nav-bar-li">
          <span>
          CONTACT <br>& LOCATION
          </span>
          <span>
            <i class="fas fa-phone-alt"></i>
          </span>
        </li>
        <li class="nav-bar-li">
          <span style="background:red;">
            DELIVERY
          </span>
          <span style="background:white;justify-content:start;">
            <i class="fas fa-biking fa-2x"></i>
          </span>
        </li>
         <li class="nav-bar-li social-media">
          <span >
          Follow us on Social Media
          <a href="https://www.instagram.com/billybob_oviedo/"><img src="../assets/images/ig.svg" class="nav-bar-icon"></a>
          <a href="https://www.facebook.com/pg/BillyBobOviedo/about/?ref=page_internal"><img src="../assets/images/fb.png" class="nav-bar-icon"></a>
          </span>
        </li>
      </ul>
      <div class="language-div">
        <img src="../assets/images/sp.png" style="width:28px; margin-right:10px">
        <img src="../assets/images/usa.png" style="width:24px;margin-bottom:2px">
      </div>
    </nav>
</template>
<script>
import moment from 'moment/moment';

export default {
  name: 'NavBar',
  data() {
    return {
      changeLogo: true,
      isOpen: moment().isBetween(moment('20:00:00', 'HH:mm:ss'), moment('23:59:59', 'HH:mm:ss')),
      time: this.calculareDiff(),
    };
  },
  methods: {
    calculareDiff() {
      this.fmsToHMS(moment().clone().endOf('day').add(-4, 'hours')
        .diff(moment()));
    },
    fmsToHMS(ms) {
      let seconds = ms / 1000;
      const hours = parseInt((ms / 1000) / 3600, 10);
      seconds %= 3600;
      const minutes = parseInt(seconds / 60, 10);
      seconds %= 60;
      this.time = (`${hours}:${minutes}:${Math.trunc(seconds)}`);
    },
  },
  mounted() {
    this.timer = setInterval(() => this.calculareDiff(), 1000);
  },
  beforeDestroy() {
    clearInterval(this.timer);
  },
};
</script>

<style scoped>
/**************GLOBALS***************/
.nav-bar{
z-index: 3;
display:flex;
align-items: center;
justify-content: center;
height:100px;
color:white;
font-weight: 600;
font-size:20px;
background: black;
position: fixed;
width: 100%;
top:0;
}
@media screen and (max-width: 1350px) {
  .nav-bar{
  font-size:12px;
  }
  li{
  width:100px !important;
  margin: 0px 5px !important
  }
}
@media screen and (max-width: 860px) {
  .open,.close,.social-media{
  display:none;
  }
}
@media screen and (max-width: 400px) {
  li{
  margin: 0px !important
  }
}
.language-div{
  font-size:14px;
  position: absolute;
  right:26px;
  top: 0;
}
/* a,a.unvisited, a.unvisited:visited, a.unvisited:active{
  text-decoration: none;
  color:white;
  position: relative;
  z-index: 10;
} */
/**************HOME BUTTON***************/
.home-button{
  cursor:pointer;
  background: url('~@/assets/images/logo.jpg') no-repeat;
   background-size: contain;
  width:170px;
  height:170px;
  position: absolute;
  top:10px;
  border-radius: 110px;
  outline:none;
  border:2px solid black;
  z-index: 5;
}
.american{
 background-size: 120% !important;
 background-position: center !important;
  background: url('~@/assets/images/logo3.jpg') no-repeat;
}
.home-button:hover{
width:182px;
height:182px;
}
/**************NAVIGATION***************/
.nav-bar-left{
margin:30px 90px 0px 0px;
display:flex;
text-align: center;
flex:1;
justify-content: flex-end;
align-items: center;
padding:0;
}
.nav-bar-right{
margin:30px 0px 0px 90px;
display:flex;
text-align: center;
flex:1;
justify-content: flex-start;
padding:0;
align-items: center;
}
.nav-bar-li{
  list-style-type: none;
  height:60px;
  width:140px;
  overflow: hidden;
  z-index: 15;
  cursor: pointer;
  margin:0px 30px 10px 30px;
}
.nav-bar-li>span{
  display:flex;
  height:100%;
  width:100%;
  justify-content: center;
  align-items: center;
  text-align: center;
  transition: 0.5s;
}
.nav-bar-li>span:nth-child(1){
  color:white;
}
.nav-bar-li>span:nth-child(2){
 background: #F9C00E;
  color:black;
}
.nav-bar-li:hover span{
  transform:translateY(-100%)
}
.nav-bar-li:hover .svg-inline--fa.fa-biking.fa-w-20.fa-2x{
  transform:translateX(300%);
  transition: 4s;
}
/*******OPEN-CLOSE**********/
.open{
  cursor:default;
  border: 2px solid rgb(243, 97, 199);
  color: #fff;
  text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #ff00de, 0 0 25px #ff00de;
  -webkit-text-fill-color: #F4ECFF;
  -webkit-text-stroke-color:#C546F7;
  -webkit-text-stroke-width:0.2px;
}
.open:hover span{
  transform:none;
}
.close{
  cursor:default;
  border: 2px solid rgb(105, 202, 235) ;
  color: #fff;
  text-shadow:
    0 0 5px #fff,
    0 0 10px #fff,
    0 0 20px #fff,
    0 0 40px #0ff,
    0 0 80px #0ff,
    0 0 90px #0ff,
    0 0 100px #0ff,
    0 0 150px #0ff;
}
.close>span{
  display: block;
  padding-top: 7px;
}
.close:hover span{
  transform:none;
}

/**************SOCIAL-MEDIA***************/
.nav-bar-icon{
  width:25px;
  margin: 0 3px;
}
.social-media{
  font-size: 10px;
  border: 1px solid #F9C00E;
  cursor:default;
}
 .social-media:hover span{
  transform:none;
}
</style>
