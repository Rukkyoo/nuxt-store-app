<script setup lang="ts">
interface Product {
  id: number;
  title: string;
  price: number;
  image: string;
}

const {
  data: products,
  pending,
  error,
} = await useFetch<Product[]>("https://fakestoreapi.com/products", {
  retry: 1,
  server: true,
});
</script>

<template>
  <div class="home">
    <h1>Welcome to Rukky's Web Store!</h1>
    <p>Explore our wide range of products and find the best deals.</p>
    <div class="product-list">
      <template v-if="pending">
        <p class="status">Loading products...</p>
      </template>
      <template v-else-if="error">
        <p class="status error">
          Unable to load products. Please try again later.
        </p>
      </template>
      <template v-else>
        <ProductCard :products="products || []" />
      </template>
    </div>
  </div>
</template>

<style scoped>
.home {
  padding: 20px;
  background-color: #f5f5f5;
}
.product-list {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  gap: 20px;
  margin-top: 20px;
  background-color: #fff;
  padding: 20px;
}
.status {
  width: 100%;
  text-align: center;
  margin: 20px 0;
}
.status.error {
  color: #b00020;
}
</style>
