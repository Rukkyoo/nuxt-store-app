<template>
  <div class="home">
    <h1>Welcome to Rukky's Web Store!</h1>
    <p>Explore our wide range of products and find the best deals.</p>
    <div class="product-list">
      <ProductCard />
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
</style>
