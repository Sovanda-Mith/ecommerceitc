<template>
  <button class="btn" :class="colorClass">
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
      default: "primary",
    },
  },
  computed: {
    colorClass() {
      return `btn-${this.color}`;
    },
  },
};
</script>

<style scoped>
.btn {
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

.btn-primary {
  color: #fff;
  background-color: #007bff;
  border-color: #007bff;
}

.btn-primary:hover,
.btn-primary:focus {
  color: #fff;
  background-color: #0056b3;
  border-color: #007bff;
  outline: none;
  box-shadow: none;
}

.btn-warning {
  color: #fff;
  background-color: #fdc040;
  border-color: #fdc040;
}

.btn-warning:hover,
.btn-warning:focus {
  color: #fff;
  background-color: #e0a800;
  border-color: #ffc107;
  outline: none;
  box-shadow: none;
}

.btn-success {
  color: #fff;
  background-color: #3bb77e;
  border-color: #4bb77e;
}

.btn-success:hover,
.btn-success:focus {
  color: #fff;
  background-color: #4cb74c;
  border-color: #5cb85c;
  outline: none;
  box-shadow: none;
}
</style>
