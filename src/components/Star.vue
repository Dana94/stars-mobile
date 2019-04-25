<template>
  <div id="container">
    <div class="string"></div>
    <div id="star-five"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.string {
  height: 220px;
  width: 10px;
  background-color: saddlebrown;
  margin: 0 auto;
  position: relative;
}

/* Star shape from https://css-tricks.com/the-shapes-of-css/ */
#star-five {
  margin: 50px 0;
  position: relative;
  display: block;
  color: #f2c80f;
  width: 0px;
  height: 0px;
  border-right: 100px solid transparent;
  border-bottom: 70px solid #f2c80f;
  border-left: 100px solid transparent;
  transform: rotate(35deg);

  /* position: absolute;
  left: 36.5%;
  top: 16rem; */
}
#star-five:before {
  border-bottom: 80px solid #f2c80f;
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  position: absolute;
  height: 0;
  width: 0;
  top: -45px;
  left: -65px;
  display: block;
  content: "";
  transform: rotate(-35deg);
}
#star-five:after {
  position: absolute;
  display: block;
  color: #f2c80f;
  top: 3px;
  left: -105px;
  width: 0px;
  height: 0px;
  border-right: 100px solid transparent;
  border-bottom: 70px solid #f2c80f;
  border-left: 100px solid transparent;
  transform: rotate(-70deg);
  content: "";
}
</style>
