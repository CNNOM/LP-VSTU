<template>
  <header class="header">
    <div class="header-icon">
      <img src="../assets/img/VSTU-logo-white.png" alt="">
    </div>
    <div
        class="header-items"
        v-for="title in title"
    >
      {{ title }}
    </div>
  </header>
</template>

<script>

export default {
  components: {},

  data() {
    return {
      title: {
        0: "Обучение",
        1: "Поступление",
        2: "О нас",
        3: "Споносры",
      }
    }
  }


}
</script>

<style lang="scss" scoped>

header {
  width: 100vw;
  position: absolute;
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 1em;
  z-index: 1000;

  font-family: 'Open Sans', sans-serif;


}

.header-icon {
  justify-content: left;
}

.header-icon img {
  height: 15vh;
  width: 15vh;

}

.header-items {
  color: white;
}
</style>