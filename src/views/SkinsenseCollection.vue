<template>
  <div>
    <v-container fluid class="gradient-background">
      <h1 class="text-center font-weight-black" style="margin-bottom: 50px;">Skinsense Collection</h1>

      <div class="d-flex flex-wrap justify-space-around">
        <category-card
          title="Normal Skin"
          description="Normal skin, neither dry nor oily, A perfect balance, a canvas so holy."
          button-color="#C51162"
          button-link="/skinsense-collection/normal-skin"
          card-class="normal-skin"
        />
        <category-card
          title="Oily Skin"
          description="Oil slicked and gleaming bright, Shiny and dewy, a complexion of might."
          button-color="#C51162"
          button-link="/skinsense-collection/oily-skin"
          card-class="oily-skin"
        />
        <category-card
          title="Dry Skin"
          description="Dry skin, a canvas parched and cracked, Yearns for nourishment to bring it back."
          button-color="#C51162"
          button-link="/skinsense-collection/dry-skin"
          card-class="dry-skin"
        />
        <category-card
          title="Mature Skin"
          description="With lines etched by time, Mature skin shines like a pearl sublime."
          button-color="#C51162"
          button-link="/skinsense-collection/mature-skin"
          card-class="mature-skin"
        />
      </div>
    </v-container>
  </div>
</template>

<script>
import CategoryCard from '@/components/CategoryCard.vue';

export default {
  name: 'SkinsenseCollection',
  components: {
    CategoryCard
  },
  // add any necessary data or methods here
}
</script>

<style>

.gradient-background {
  background: linear-gradient(to right, #ffffff, #ff69b4);
}

</style>
