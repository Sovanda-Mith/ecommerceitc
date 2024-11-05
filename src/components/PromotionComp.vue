<template>
  <div class="card">
    <div class="textSection">
      <h1 class="text">{{ title }}</h1>
      <ButtonComp :color="btnColor" class="btn-row" />
    </div>
    <img :src="imgPath" alt="banner" />
  </div>
</template>

<script>
import ButtonComp from "./ButtonComp.vue";
export default {
  components: {
    ButtonComp,
  },
  props: {
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
  },
};
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
  justify-content: space-between;
  gap: 25px;
  width: 271px;
  height: 146px;
  color: #253d3e;
  position: relative;
  top: -20px;
  left: 45px;
}

.text {
  position: absolute;
  font-size: 24px;
  margin: 0;
  width: 271px;
  height: 92px;
}

.btn-row {
  position: absolute;
  top: 130px;
}
</style>
