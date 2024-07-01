<template>
  <div class="info-block">
    <div class="content">
      <div class="header">
        <a>{{ number }}</a>
        <img :src="imageSrc" :alt="text">
      </div>
      <div class="line"></div>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfoBlock',
  props: {
    number: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    imageSrc: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.info-block {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding-left: 1em;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: left;
  text-align: center;
  color: white;

}

.header {
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bolder;
  font-size: 3em;
}

.header a {
  margin-right: 15px;
}

.line {
  width: 100%;
  height: 2px;
  background-color: #E5D283;
  margin: 10px 0;
}

img {
  margin-top: 0;
  height: 70px;
  width: 70px;
}
</style>