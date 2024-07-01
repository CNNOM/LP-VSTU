<template>
  <div class="page-contain">
    <div class="in-number">
      Спонсоры
    </div>
    <div class="containers">
      <div class="container" >
        <div class="card" v-for="(item, index) in items" :key="index" >
          <div class="face face1">
            <div class="content">
              <img :src="item.imageSrc" :alt="item.text">
              <h3>{{ item.title }}</h3>
            </div>
          </div>
          <div class="face face2">
            <div class="content">
              <p>{{ item.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="containers">
      <div class="container" >
        <div class="card" v-for="(item, index) in items2" :key="index">
          <div class="face face1">
            <div class="content">
              <img :src="item.imageSrc" :alt="item.text">
              <h3>{{ item.title }}</h3>
            </div>
          </div>
          <div class="face face2">
            <div class="content">
              <p>{{ item.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import logo1 from "@/assets/img/sponsors/logo.svg"
import logo2 from "@/assets/img/sponsors/logo.png"
import logo3 from "@/assets/img/sponsors/25ff8dd1-0d1b-4cd1-9b12-42aad332916c.0012797418-Photoroom.png"
import logo4 from "@/assets/img/sponsors/brand.png"
import logo5 from "@/assets/img/sponsors/logo_niiet.png"
import logo6 from "@/assets/img/sponsors/i-2CLUhu_g8-transformed.webp"
export default {
  data() {
    return {
      items: [
        { imageSrc: logo1, title: '«Рубеж»', text: 'Рубеж - технологическая компания, занимающаяся разработкой и производством средств связи, электронных систем управления и мониторинга. Выпускники ВГТУ могут найти интересную работу в этой компании. '},
        { imageSrc: logo2, title: 'ВЭПИ', text:'ВЭПИ (Воронежский экономико-правовой институт) - вуз, готовящий специалистов в области экономики, права и управления. Некоторые выпускники ВГТУ могут продолжить обучение в ВЭПИ.' },
        { imageSrc: logo3, title: 'ВАСО' , text:'ВАСО - крупное авиастроительное предприятие, производящее и обслуживающее гражданские и военные самолеты. Выпускники ВГТУ технических специальностей могут найти интересную работу в ВАСО.' },
      ],
      items2:[
        { imageSrc: logo4, title: '"Статус Групп"', text:'ООО "Статус Групп" - динамично развивающаяся компания, занимающаяся строительством и проектированием недвижимости.' },
        { imageSrc: logo5, title: 'АО «НИИЭТ»', text:'АО «НИИЭТ» - ведущее предприятие в области разработки и производства электронной компонентной базы. Выпускники ВГТУ технических специальностей могут найти интересную работу в АО «НИИЭТ».'  },
        { imageSrc: logo6, title: 'МГСУ' , text:'МГСУ (Московский государственный строительный университет) - это один из ведущих строительных вузов в России. Некоторые выпускники ВГТУ могут продолжить свое образование в МГСУ.' },
      ]
    };
  }
}
</script>

<style lang="scss" scoped>
.page-contain {
  align-items: center;
  justify-content: center;
  background: #F0F0F0;
  font-family: 'Open Sans', sans-serif;
  margin: 0 auto;
  padding: 0;

}

.in-number{
  position: relative;
  text-align: center;
  font-size: 34px;
  font-weight: 200;
  line-height: 2;
  color: #2c3e50;
  margin: 15vh 15vh 5vh;
}

.containers{
  display: flex;
  justify-content: center;
  align-items: center;
}

.container{
  width: 1000px;
  position: relative;
  display: flex;
  justify-content: space-between;
}

.container .card{
  position: relative;
  cursor: pointer;
}

.container .card .face{
  width: 300px;
  height: 200px;
  transition: 0.5s;
}

.container .card .face.face1{
  position: relative;
  background: #213555;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transform: translateY(100px);
}

.container .card:hover .face.face1{
  background: #E5D283;
  transform: translateY(0);
}

.container .card .face.face1 .content{
  opacity: 0.2;
  transition: 0.5s;
}

.container .card:hover .face.face1 .content{
  opacity: 1;
}
.content img{
  width: 100%;
  height: 100%;
}
.container .card .face.face1 .content img{
  max-width: 150px;
  max-height: 150px;
  min-width:100px;


}

.container .card .face.face1 .content h3{
  margin: 10px 0 0;
  padding: 0;
  color: #fff;
  text-align: center;
  font-size: 1.5em;
}

.container .card .face.face2{
  position: relative;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.8);
  transform: translateY(-100px);
}

.container .card:hover .face.face2{
  transform: translateY(0);
}

.container .card .face.face2 .content p{
  margin: 0;
  padding: 0;
}

.container .card .face.face2 .content a{
  margin: 15px 0 0;
  display:  inline-block;
  text-decoration: none;
  font-weight: 900;
  color: #333;
  padding: 5px;
  border: 1px solid #333;
}

.container .card .face.face2 .content a:hover{
  background: #333;
  color: #fff;
}

</style>