<template>
    <div class="footer">
    <div class="footer-div">
      <div class="footer-cards">
        <p class="titles-bottom-cards">OPENING HOURS</p>
        <br>
        <p>SUND-THU______________20:00-00:00</p>
        <p>FRI-SAT________________20:00-00:30</p>
      </div>
      <div class="footer-cards">
        <p class="titles-bottom-cards">LOCATIONS</p>
        <br>
        <p>Calle Fray Ceferino, 11, 33001 Oviedo, Asturias</p>
        <p>Calle Magdalena, 20, 33009 Oviedo, Asturias</p>
      </div>
      <div class="footer-cards">
        <p class="titles-bottom-cards">CONTACT</p>
        <br>
        <p>984 49 63 02 <i class="fas fa-phone-alt"></i></p>
        <p>billyboboviedo@gmail.com <i class="fas fa-envelope solid"></i></p>
      </div>
      <div class=bottom-logo></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer{
  background: black;
  color:white;
  width:100%;
}
.footer-div{
  padding:2em;
  display:flex;
  justify-content: flex-end;
  align-items: center;
}
.footer-cards{
  font-size: 12px;
  margin-right:40px;
}
.titles-bottom-cards{
  font-size:14px;
  font-weight: bold;
}
.bottom-logo{
  padding:0;
  width:170px;
  height:170px;
  background-size: 120% !important;
 background-position: center !important;
  background: url('~@/assets/images/logo3.jpg') no-repeat;
  border-radius: 110px;
}
</style>
