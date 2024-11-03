<template>
  <div class="category">
    <img :src="props.imgPath" alt="category picture" />
    <div class="title">
      <h1>{{ props.title || "Placeholder" }}</h1>
      <p>{{ props.amount }} Items</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  imgPath: {
    type: String,
  },
  title: {
    type: String,
  },
  amount: {
    type: Number,
  },
  bgColor: {
    type: String,
  },
});
</script>

<style scoped>
.title {
  font-family: Quicksand;
  font-weight: 700;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: start;
}

.category {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: start;
  background-color: v-bind(bgColor);
  width: 136px;
  height: 177px;
  border: #81b13d solid 1px;
  border-radius: 10px;
}
.category img {
  width: 120px;
  height: 120px;
}
.category div {
  height: 39px;
  font-size: 12px;
}

.category div h1 {
  font-size: 16px;
  height: 29px;
  color: #253d4e;
  margin: 0;
}

.category div p {
  font-size: 12px;
  color: #b6b6b6;
  margin: 0;
}
</style>
