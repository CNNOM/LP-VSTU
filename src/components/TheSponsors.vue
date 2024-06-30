<template>
  <div class="in-number">
    Спонсоры
  </div>
  <div class="grid-container">
    <div class="grid-item" v-for="(item, index) in items" :key="index">
      <div class="circle">
        <img :src="item.imageSrc" :alt="item.text">
      </div>
      <p>{{ item.text }}</p>
    </div>
  </div>
</template>


<script>
import logo1 from "@/assets/img/sponsors/logo.svg"
import logo2 from "@/assets/img/sponsors/logo.png"
import logo3 from "@/assets/img/sponsors/25ff8dd1-0d1b-4cd1-9b12-42aad332916c.0012797418.png"
import logo4 from "@/assets/img/sponsors/brand.png"
import logo5 from "@/assets/img/sponsors/logo_niiet.png"
import logo6 from "@/assets/img/sponsors/logomgsu.svg"
export default {
  data() {
    return {
      items: [
        { imageSrc: logo1, text: 'Группа компаний «Рубеж»' },
        { imageSrc: logo2, text: 'Воронежский экономико-правовой институт' },
        { imageSrc: logo3, text: 'Воронежское акционерное самолетостроительное общество' },
        { imageSrc: logo4, text: 'ООО "Статус Групп"' },
        { imageSrc: logo5, text: 'АО «НИИЭТ»' },
        { imageSrc: logo6, text: 'Национальный исследовательский Московский государственный строительный университет' },
      ]
    };
  }
}
</script>

<style lang="scss" scoped>
.in-number{
  text-align: center;
  font-size: 34px;
  font-weight: 200;
  line-height: 2;
  color: #2c3e50;
  margin: 15vh 15vh 5vh;
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.grid-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.circle {
  height: 200px;
  width: 300px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f0f0f0;
  border-radius: 25px;
  border: 1px solid #E5D283;
  padding: 5px;
}

.circle img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

p {
  margin-top: 10px;
  font-size: 24px;
  font-weight: 200;
  line-height: 2;
  color: #2c3e50;
}
</style>