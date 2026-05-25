<script setup lang="ts">
interface Product {
  id: number;
  title: string;
  price: number;
  description: string;
  image: string;
}

const route = useRoute();
const { data: product } = await useFetch<Product>(
  `https://fakestoreapi.com/products/${route.params.id}`,
);
</script>

<template>
  <div v-if="product" class="product-details">
    <img :src="product.image" :alt="product.title" class="product-image" />
    <div class="product-info">
      <h1>{{ product.title }}</h1>
      <p class="price">${{ product.price }}</p>
      <p>
        {{ product.description }}
      </p>
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
