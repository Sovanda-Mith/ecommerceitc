<template>
  <button class="btn">
    Shop Now
    <img
      src="@/assets/right-arrow-7359.svg"
      alt="right arrow icon"
      style="width: 15px"
    />
  </button>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "#3bb77e",
    },
  },
};
</script>

<style scoped>
.btn {
  color: #fff;
  background-color: v-bind(color);
  border-color: v-bind(color);
  font-family: Quicksand;
  font-weight: 700;
  font-size: 14px;
  display: flex;
  align-items: center;
  gap: 10px;
  border-radius: 3px;
  width: fit-content;
  padding: 8px 15px;
  cursor: pointer;
}
</style>
