<template>
  <div class="card">
    <div class="textSection">
      <h1>{{ props.title }}</h1>
      <ButtonComp :color="props.btnColor" />
    </div>
    <img :src="props.imgPath" alt="banner" />
  </div>
</template>

<script setup>
import ButtonComp from "./ButtonComp.vue";
const props = defineProps({
  imgPath: {
    type: String,
    default: "../src/assets/onion.png",
  },
  btnColor: {
    type: String,
    default: "primary",
  },
  title: {
    type: String,
  },
  bgColor: {
    type: String,
  },
});
</script>

<style scoped>
.card {
  display: flex;
  align-items: center;
  width: 512px;
  height: 300px;
  border-radius: 10px;
  background-color: v-bind(bgColor);
}

.card img {
  width: 250px;
  position: relative;
  bottom: -10px;
  right: 15px;
}

.textSection {
  font-family: Quicksand;
  font-weight: 700;
  display: flex;
  flex-direction: column;
  gap: 25px;
  width: 271px;
  height: 146px;
  color: #253d3e;
  position: relative;
  top: -20px;
  left: 45px;
}

.textSection h1 {
  font-size: 24px;
  width: 271px;
  height: 92px;
}
</style>
