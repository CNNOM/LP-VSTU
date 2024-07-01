<template>
  <div class="page-contain">
    <h1>
      Поступление в ВГТУ
    </h1>
    <div class="ag-format-container">
      <div class="ag-courses_box">
        <div
            class="ag-courses_item"
             v-for="title in title"
        >
          <a :href="url in links"
              class="ag-courses-item_link"
          >
            <div class="ag-courses-item_bg">
            </div>
            <div
                class="ag-courses-item_title"
            >
              {{ title }}
            </div>
          </a>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      title:{
        0: "Среднее профессиональное образование",
        1: "Бакалавриат и специалитет",
        2: "Магистратура",
        3: "Аспирантура",
        4: "Целевое обучение",
        5: "Военный учебный центр",
        6: "Информационные материалы",
        7: "Иностранным абитуриентам",
        8: "Об общежитиях",
      },
      links:{
        0: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/spo/",
        1: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/bak-spec/",
        2: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/mag/",
        3: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/asp/",
        4: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/tselevoi-priem/",
        5: "https://cchgeu.ru/education/military/",
        6: "https://cchgeu.ru/education/military/",
        7: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/inostr/",
        8: "https://abiturient.cchgeu.ru/osnovnye-svedeniya-postupayushchim/obshchezhitiya.php",
      }
    }
  }
}

</script>

<style lang="scss" scoped>


.page-contain {
  min-height: 85vh;
  align-items: center;
  justify-content: center;
  background: #F0F0F0;
  padding: 2em;
  font-family: 'Open Sans', sans-serif;
  margin: 0 auto;
}

.ag-format-container {
  width: 1142px;
  margin: 0 auto;
}

h1{
  text-align: center;
  font-size: 34px;
  font-weight: 200;
  line-height: 2;
  color: #2c3e50;
}

.ag-courses_box {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: start;
  -ms-flex-align: start;
  align-items: flex-start;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;

  padding: 50px 0;

}

.ag-courses_item {
  -ms-flex-preferred-size: calc(33.33333% - 30px);
  flex-basis: calc(33.33333% - 30px);

  margin: 0 15px 30px;

  overflow: hidden;

  border-radius: 28px;

}

.ag-courses-item_link {
  display: block;
  padding: 30px 20px;
  background-color: #213555;


  overflow: hidden;

  position: relative;
  text-decoration: none;

}




.ag-courses-item_link:hover,
.ag-courses-item_link:hover .ag-courses-item_date {
  color: #FFF;

}


.ag-courses-item_link:hover .ag-courses-item_bg {
  -webkit-transform: scale(10);
  -ms-transform: scale(10);
  transform: scale(10);
}

.ag-courses-item_title {
  min-height: 87px;
  margin: 0 0 25px;

  overflow: hidden;

  font-weight: bold;
  font-size: 30px;
  color: #FFF;
  z-index: 2;
  position: relative;
}



.ag-courses-item_date-box {
  font-size: 18px;
  color: #FFF;

  z-index: 2;
  position: relative;
}

.ag-courses-item_bg {
  height: 128px;
  width: 128px;
  background-color: #E5D283;

  z-index: 1;
  position: absolute;
  top: -75px;
  right: -75px;

  border-radius: 50%;

  -webkit-transition: all .5s ease;
  -o-transition: all .5s ease;
  transition: all .5s ease;
}

//.ag-courses_item:nth-child(2n) .ag-courses-item_bg {
//  background-color: #213555;
//}

//.ag-courses_item:nth-child(3n) .ag-courses-item_bg {
//  background-color: #e44002;
//}
//
//.ag-courses_item:nth-child(4n) .ag-courses-item_bg {
//  background-color: #952aff;
//}
//
//.ag-courses_item:nth-child(5n) .ag-courses-item_bg {
//  background-color: #cd3e94;
//}
//
//.ag-courses_item:nth-child(6n) .ag-courses-item_bg {
//  background-color: #4c49ea;
//}


@media only screen and (max-width: 979px) {
  .ag-courses_item {
    -ms-flex-preferred-size: calc(50% - 30px);
    flex-basis: calc(50% - 30px);
  }
  .ag-courses-item_title {
    font-size: 24px;
  }
}

@media only screen and (max-width: 767px) {
  .ag-format-container {
    width: 96%;
  }

}

@media only screen and (max-width: 639px) {
  .ag-courses_item {
    -ms-flex-preferred-size: 100%;
    flex-basis: 100%;
  }
  .ag-courses-item_title {
    min-height: 72px;
    line-height: 1;

    font-size: 24px;
  }
  .ag-courses-item_link {
    padding: 22px 40px;
  }
  .ag-courses-item_date-box {
    font-size: 16px;
  }
}
</style>