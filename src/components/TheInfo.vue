<template>
  <div class="page-header">
    <div class="left">

    </div>
    <div class="right">
      <div class="right-2">

      </div>
      <div class="right-3">

      </div>
      <div class="right-5">

      </div>
    </div>
    <!--    <div class="right-4">-->

    <!--    </div>-->
    <div class="text">
      <h1>
        ВГТУ – твой первый приоритет!
      </h1>
      <div class="line"></div>
      <a>
        Воронежский государственный технический университет – опорный вуз региона. Статус опорного университет получил в 2016 году, войдя в число первых 11 победителей конкурса Минобрнауки РФ и объединившись с Воронежским государственным архитектурно-строительным университетом. Вобрав в себя образовательный, научный, кадровый и материально-технический потенциал двух ведущих технических вузов области
      </a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>

.page-header {
  font-family: Noto Sans, sans-serif;
  position: relative;
  display: flex;
  height: 80vh;
  margin: 10%;
  border: 2px solid #E5D283;
  border-radius: 30px;
  background: #F0F0F0;
}

.left {
  height: 100%;
  //background-color: #213555;
  width: 40%;
}

.right {
  height: 100%;
  width: 60%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}

.right-2 {
  background-image: url("@/assets/img/stats.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  border-radius: 50%;
  width: 500px;
  height: 500px;
  position: relative;
  z-index: 3;
}


.right-3 {
  background-color: #213555;
  border-radius: 50%;
  width: 500px;
  height: 500px;
  position: absolute;
  z-index: 1;
  transform: translateX(-100px);
}

.right-5 {
  border: 2px solid #E5D283;
  border-radius: 50%;
  width: 500px;
  height: 500px;
  position: absolute;
  z-index: 2;
  transform: translateX(50px) translateY(40px);
}


.right-4 {
  background-image: url("@/assets/img/5.svg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 2;
}

.line {
  width: 100%;
  height: 2px;
  background-color: #E5D283;
  margin: 10px 0;
}

.text {
  position: absolute;
  top: 40%;
  left: 20%;
  transform: translate(-40%, -50%);
  color: #213555;
  text-align: left;
  z-index: 4;
  width: 600px;

}

.text a{
  font-size: 20px;
  line-height: 1.5 ;
}
</style>