<template>
  <div class="featured">
    <section class="categories">
      <CategoryComp
        v-for="category in categories"
        :image="category.image"
        :name="category.name"
        :productCount="category.productCount"
        :color="category.color"
        :key="category.name"
      />
    </section>
    <section class="promotions">
      <PromotionComp
        v-for="promotion in promotions"
        :image="promotion.image"
        :title="promotion.title"
        :buttonColor="promotion.buttonColor"
        :color="promotion.color"
        :key="promotion.title"
      />
    </section>
  </div>
</template>
<script>
import axios from "axios";
import CategoryComp from "./components/CategoryComp.vue";
import PromotionComp from "./components/PromotionComp.vue";
export default {
  data() {
    return {
      promotions: [],
      categories: [],
    };
  },
  components: {
    CategoryComp,
    PromotionComp,
  },
  methods: {
    fetchCategories() {
      axios
        .get("http://localhost:3000/api/categories")
        .then((response) => {
          this.categories = response.data;
        })
        .catch((error) => {
          console.error("Error fetching data: ", error);
        });
    },
    fetchPromotions() {
      axios
        .get("http://localhost:3000/api/promotions")
        .then((response) => {
          this.promotions = response.data;
        })
        .catch((error) => {
          console.error("Error fetching data: ", error);
        });
    },
  },
  mounted() {
    this.fetchCategories();
    this.fetchPromotions();
  },
};
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
