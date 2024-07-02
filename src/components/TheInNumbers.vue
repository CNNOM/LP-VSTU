<template>
  <div class="in-number">
    ВГТУ в цифрах
  </div>
  <div class="components">
    <div class="block-60">
      <InfoBlock
          v-for="(item, index) in block60Data"
          :key="index"
          :number="item.number"
          :text="item.text"
          :imageSrc="item.imageSrc"
      />
    </div>
    <div class="block-40">
      <div class="small-block" v-for="(item, index) in block40Data" :key="index">
        <InfoBlock
            :number="item.number"
            :text="item.text"
            :imageSrc="item.imageSrc"
        />
      </div>
    </div>
  </div>
</template>

<script>
import InfoBlock from "@/components/number/InfoBlock.vue";
import peple from  '@/assets/img/peple.svg'
import volunteer from  '@/assets/img/volunteer.svg'
import laboratory from  '@/assets/img/Laboratorys.svg'
import event from  '@/assets/img/event.svg'
import project from  '@/assets/img/Project.svg'
import science from  '@/assets/img/Science.svg'
import loc from  '@/assets/img/loc.svg'



export default {
  components: {InfoBlock},
  data() {
    return {
      block60Data: [
        { number: 20000, text: "Студентов", imageSrc: peple }
      ],
      block40Data: [
        { number: 2000, text: "Волонтеров", imageSrc: volunteer },
        { number: 3000, text: "Бюджетных мест", imageSrc: loc },
        { number: 400, text: "Мероприятий в год", imageSrc: event },
        { number: 100, text: "Лабораторий", imageSrc: laboratory },
        { number: 50, text: "Реализуемых проектов", imageSrc: project },
        { number: 35, text: "Научных направлений", imageSrc: science },
      ]
    };
  }
}
</script>

<style lang="scss" scoped>
.components {
  margin-left: 10%;
  margin-right: 10%;
  padding: 0;
  display: flex;
  height: 70vh;
  border-radius: 25%;
  margin-bottom: 5%;
  font-family: 'Open Sans', sans-serif;

}
.block-60 {
  width: 50%;
  background-color: #4F709C;
  display:block;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  padding-top: 20vh;
}
img{
  width: 10vh;
  height: 10vh;
}

.in-number{
  font-family: 'Open Sans', sans-serif;

  text-align: center;
  font-size: 34px;
  font-weight: 200;
  line-height: 2;
  color: #2c3e50;
  margin-top: 5%;
  margin-bottom: 2%;
}
.block-40 {
  width: 50%;
  display: flex;
  flex-wrap: wrap;
}
.small-block {
  width: 50%;
  height: 33.33%;
  display: flex;
  align-items: center;
  justify-content: left;
  font-size: 18px;
}

.small-block:nth-child(1) { background-color: #516a8f; width: 40%;}
.small-block:nth-child(2) { background-color: #213555; width: 60%;}
.small-block:nth-child(3) { background-color: #668dbd; width: 40%;}
.small-block:nth-child(4) { background-color: #374a6a; width: 60%;}
.small-block:nth-child(5) { background-color: #3d618f; width: 40%;}
.small-block:nth-child(6) { background-color: #668dbd; width: 60%;}
</style>