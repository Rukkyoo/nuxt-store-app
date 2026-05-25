<script setup lang="ts">
import type { Product } from '../../../types/product'
</script>

<template>
  <div class="product-details">
    <img :src="" :alt="" class="product-image" /> <!-- Product Image goes here -->
    <div class="product-info">
      <h1></h1> <!-- Product Title goes here -->
      <p class="price"></p> <!-- Product Price goes here -->
      <p></p> <!-- Product Description goes here -->
    </div>
  </div>
</template>

<style scoped>
.product-details {
  display: flex;
  gap: 40px;
  padding: 40px;
  flex-wrap: wrap;
}
.product-image {
  width: 300px;
  height: 300px;
  object-fit: contain;
}
.product-info {
  flex: 1;
  min-width: 250px;
}
.price {
  font-size: 24px;
  font-weight: bold;
  margin: 20px 0;
}
@media (max-width: 768px) {
  .product-details {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .product-image {
    width: 220px;
    height: 220px;
  }
}
</style>
