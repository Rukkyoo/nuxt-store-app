<script setup lang="ts">
const { data } = await useFetch('https://fakestoreapi.com/products') 
console.log(data)

</script>

<template>
    <div v-for="product in data" :key="product.id" class="product-card">
        <img :src="product.image" class="product-image" :alt="product.title" />
        <p class="product-title">{{ product.title }} - ${{  product.price  }}</p>
        <Button />
    </div>
</template>

<style scoped>

.product-card {
  width: 40vw;
  padding: 10px 10px 10px 10px;
  border: 2px solid #ccc;
  border-radius: 5px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.product-image {
  width: 50%;
}

.product-title {
  font-size: 14px;
}
</style>