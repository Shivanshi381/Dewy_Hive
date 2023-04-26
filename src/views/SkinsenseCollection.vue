<template>
  <div>
    <h1 class="text-center">Skinsense Collection</h1>
    <div class="d-flex flex-wrap justify-space-around">
      <div class="category-card normal-skin">
        <h2 class="text-center">Normal Skin</h2>
        <p class="text-center">Normal skin, neither dry nor oily,
           A perfect balance, a canvas so holy.</p>
           <br>
           <p class="text-center">Let's Explore products specially curated for your skin!</p>
           <v-row justify="center">
  <v-btn color="#800080" to="/skinsense-collection/normal-skin">Shop Now</v-btn>
</v-row>

      </div>
      <div class="category-card oily-skin">
        <h2 class="text-center">Oily Skin</h2>
        <p class="text-center">Oil slicked and gleaming bright,
           Shiny and dewy, a complexion of might.</p>
           <br>
           <p class="text-center">Let's Explore products specially curated for your skin!</p>
           <v-row justify="center">
  <v-btn color="#800080" to="/skinsense-collection/oily-skin">Shop Now</v-btn>
</v-row>

      </div>
      <div class="category-card dry-skin">
        <h2 class="text-center">Dry Skin</h2>
        <p class="text-center">Dry skin, a canvas parched and cracked,
           Yearns for nourishment to bring it back.</p>
           <br>
           <p class="text-center">Let's Explore products specially curated for your skin!</p>
           <v-row justify="center">
  <v-btn color="#800080" to="/skinsense-collection/dry-skin">Shop Now</v-btn>
</v-row>

      </div>
      <div class="category-card mature-skin">
        <h2 class="text-center">Mature Skin</h2>
        <p class="text-center">With lines etched by time,
           Mature skin shines like a pearl sublime.</p>
          <br>
          <p class="text-center">Let's Explore products specially curated for your skin!</p>
          <v-row justify="center">
  <v-btn color="#800080" to="/skinsense-collection/mature-skin">Shop Now</v-btn>
</v-row>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkinsenseCollection',
  // add any necessary data or methods here
}
</script>

<style>
.category-card {
  background-color: #FFC0CB;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  padding: 1rem;
  width: 300px;
  margin: 1rem;
}

.category-card h2 {
  margin-top: 0;
}

.category-card p {
  margin-bottom: 1rem;
}
</style>
