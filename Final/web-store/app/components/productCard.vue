<script setup lang="ts">
const { data } = await useFetch("https://fakestoreapi.com/products");

console.log(data);
</script>

<template>
  <div class="products-container">
    <div v-for="product in data" :key="product.id" class="product-card">
      <img :src="product.image" class="product-image" :alt="product.title" />

      <p class="product-title">
        {{ product.title }}
      </p>

      <p class="product-price">${{ product.price }}</p>

      <button class="product-button">View Product</button>
    </div>
  </div>
</template>

<style scoped>
.products-container {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  padding: 20px;
}

.product-card {
  background: white;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 16px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

.product-image {
  width: 100%;
  height: 220px;
  object-fit: contain;
}

.product-title {
  font-size: 14px;
  margin-top: 10px;
  text-align: center;
  overflow: hidden;
}

.product-price {
  font-size: 18px;
  font-weight: bold;
  margin: 10px 0;
}

.product-button {
  width: 100%;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 14px;
}

/* Tablet */
@media (max-width: 768px) {
  .products-container {
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  }

  .product-image {
    height: 180px;
  }
}

/* Mobile */
@media (max-width: 480px) {
  .products-container {
    grid-template-columns: 1fr;
    padding: 10px;
  }
  .product-card {
    padding: 12px;
  }
  .product-image {
    height: 160px;
  }
  .product-title {
    font-size: 13px;
  }
  .product-price {
    font-size: 16px;
  }
}
</style>
