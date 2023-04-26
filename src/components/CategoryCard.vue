<template>
    <div class="category-card" :class="cardClass">
      <h2 class="text-center">{{ title }}</h2>
      <p class="text-center">{{ description }}</p>
      <br>
      <p class="text-center">Let's explore products specially curated for your skin!</p>
      <v-row justify="center">
        <v-btn :color="buttonColor" :to="buttonLink">Shop Now</v-btn>
      </v-row>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CategoryCard',
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      buttonColor: {
        type: String,
        required: true
      },
      buttonLink: {
        type: String,
        required: true
      },
      cardClass: {
        type: String,
        default: ''
      }
    }
  }
  </script>
  
  <style scoped>
  .category-card {
    background-color: #e9dadd;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    padding: 1rem;
    width: 50%;
    margin: 1rem;
  }
  
  .category-card:hover {
    background-color:#cd8aae;
  }
  
  .category-card h2 {
    margin-top: 0;
  }
  
  .category-card p {
    margin-bottom: 1rem;
  }
  </style>
  