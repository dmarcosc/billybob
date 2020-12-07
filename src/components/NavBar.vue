<template>
  <nav class="nav-bar">
    <button @click="changeLogo=!changeLogo"
              :class="{ 'home-button':changeLogo , 'home-button american': !changeLogo }">
      </button>
      <ul class="nav-bar-left">
        <li>
          <span>
            OUR <br> CHALLENGE
          </span>
          <span>
            <i class="fas fa-star"></i>
          </span>
        </li>
        <li>
          <span>
            FOOD <br> & DRINK
          </span>
          <span>
            <i class="fas fa-utensils"></i>
          </span>
        </li>
      </ul>
      <ul class="nav-bar-right">
        <li>
          <span>
          CONTACT <br>& LOCATION
          </span>
          <span>
            <i class="fas fa-phone-alt"></i>
          </span>
        </li>
        <li>
          <span>
            GALLERY <br> & ABOUT
          </span>
          <span>
            <i class="fas fa-camera"></i>
          </span>
        </li>
         <li class="social-media">
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
export default {
  name: 'NavBar',
  props: {
  },
  data() {
    return {
      changeLogo: true,
    };
  },
};
</script>

<style scoped>
/**************GLOBALS***************/
.nav-bar{
display:flex;
align-items: center;
justify-content: center;
height:100px;
padding:10px;
color:white;
font-weight: 600;
font-size:20px;
background: black;
position: fixed;
width: 100%;
top:0;
}
@media screen and (max-width: 1220px) {
  .nav-bar{
  font-size:12px;
  }
  li{
  width:100px !important;
  margin: 0px 5px !important
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
  background: url(../assets/images/logo.jpg) no-repeat;
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
  background: url(../assets/images/logo3.jpg) no-repeat;
}
.home-button:hover{
width:180px;
height:180px;
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
justify-content: start;
padding:0;
align-items: center;
}
li{
  list-style-type: none;
  height:60px;
  width:140px;
  overflow: hidden;
  z-index: 15;
  cursor: pointer;
  margin:0 15px;
}
li>span{
  display:flex;
  height:100%;
  width:100%;
  justify-content: center;
  align-items: center;
  text-align: center;
  transition: 0.5s;
}
li>span:nth-child(1){
  color:white;
}
li>span:nth-child(2){
  background:yellow;
  color:black;
}
li:hover span{
  transform:translateY(-100%)
}
a{
  color:white;
}
/**************SOCIAL-MEDIA***************/
.nav-bar-icon{
  width:25px;
  margin: 0 3px;
}
.social-media{
  font-size: 10px;
  border: 1px solid yellow;
  cursor:default;
}
 .social-media:hover span{
  transform:none;
}
</style>
