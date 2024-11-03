<template>
  <div class="featured">
    <section class="categories">
      <CategoryComp
        v-for="category in categories"
        :imgPath="category.imgPath"
        :title="category.title"
        :amount="category.amount"
        :bgColor="category.bgColor"
        :key="category.title"
      />
    </section>
    <section class="promotions">
      <PromotionComp
        v-for="promotion in promotions"
        :imgPath="promotion.imgPath"
        :title="promotion.title"
        :btnColor="promotion.btnColor"
        :bgColor="promotion.bgColor"
        :key="promotion.title"
      />
    </section>
  </div>
</template>
<script setup>
import { RouterLink, RouterView } from "vue-router";
import CategoryComp from "./components/CategoryComp.vue";
import PromotionComp from "./components/PromotionComp.vue";
const categories = [
  {
    imgPath: "../src/assets/hamburger.png",
    title: "Cake & Milk",
    amount: 14,
    bgColor: "#f2fce4",
  },
  {
    imgPath: "../src/assets/peach.png",
    title: "Peach",
    amount: 17,
    bgColor: "#fffceb",
  },
  {
    imgPath: "../src/assets/kiwi.png",
    title: "Organic Kiwi",
    amount: 21,
    bgColor: "#ecffec",
  },
  {
    imgPath: "../src/assets/apple.png",
    title: "Red Apple",
    amount: 68,
    bgColor: "#feefea",
  },
  {
    imgPath: "../src/assets/snack.png",
    title: "Snack",
    amount: 34,
    bgColor: "#fff3eb",
  },
  {
    imgPath: "../src/assets/black_plum.png",
    title: "Black plum",
    amount: 25,
    bgColor: "#fff3ff",
  },
  {
    imgPath: "../src/assets/vegetable.png",
    title: "Vegetables",
    amount: 65,
    bgColor: "#f2fce4",
  },
  {
    imgPath: "../src/assets/headphone.png",
    title: "Headphone",
    amount: 33,
    bgColor: "#fffceb",
  },
  {
    imgPath: "../src/assets/cake.png",
    title: "Cake & Milk",
    amount: 54,
    bgColor: "#f2fce4",
  },
  {
    imgPath: "../src/assets/orange.png",
    title: "Orange",
    amount: 63,
    bgColor: "#fff3ff",
  },
];

const promotions = [
  {
    imgPath: "../src/assets/onion.png",
    title: "Everyday Fresh & Clean with Our Products",
    btnColor: "success",
    bgColor: "#f0e8d5",
  },
  {
    imgPath: "../src/assets/beverage.png",
    title: "Make your Breakfast Healthy and Easy",
    btnColor: "success",
    bgColor: "#f3e8e8",
  },
  {
    imgPath: "../src/assets/organic.png",
    title: "The best Organic Products Online",
    btnColor: "warning",
    bgColor: "#e7eaf3",
  },
];
</script>

<style scoped>
.featured {
  display: flex;
  flex-direction: column;
  gap: 50px;
}

.categories {
  display: flex;
  gap: 22px;
}

.promotions {
  display: flex;
  gap: 25px;
}
</style>
