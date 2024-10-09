<script setup>
import FormElement from './FormElement.vue';
import Menu from './Menu.vue';
</script>

<template>
  <div class="container">
    <!-- Title -->
    <h1 class="title">Welcome to Vietfood</h1>
    
    <!-- Paragraph with link -->
    <p class="description">
      Discover the rich and diverse flavors of Vietnam with Vietfood. Whether you're craving Pho, Banh Mi, or Bun Bo Hue, we bring authentic Vietnamese cuisine to your table. Watch our introductory video to learn more about our dishes:
      <a href="https://www.youtube.com/watch?v=WlosNFMCnE4" target="_blank">Watch Vietfood Introduction - How to make Pho</a>.
    </p>

    <!-- Image -->
    <img src="../assets/pho_vn_food.jpg" alt="Delicious Vietnamese Food" class="vietfood-image">
    <img src="../assets/bun_bo_hue_vn_food.jpg" alt="Delicious Vietnamese Food" class="vietfood-image">
    <Menu></Menu>
      <FormElement></FormElement>
  </div>
  <FormElement></FormElement>

</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
.container {
  text-align: center;
}

.title {
  font-size: 2.5em;
  margin-bottom: 20px;
}

.description {
  font-size: 1.2em;
  margin-bottom: 20px;
}

.vietfood-image {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}
</style>
