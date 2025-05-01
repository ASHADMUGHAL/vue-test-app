<template>
  <!-- Uncomment the line below to pass data or leave it to use default values -->
  <div>
    <homePage />
    <p>This is Change</p>
  </div>
  <!-- <ProductCard />  This would use default values instead of passed data -->
</template>

<script>
import homePage from "./components/homePage.vue";

export default {
  components: {
    homePage,
  },
};
</script>
