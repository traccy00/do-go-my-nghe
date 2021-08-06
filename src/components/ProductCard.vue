<template>
  <!-- <router-link class="product-link"> -->
  <!-- <div class="product-card list-item">
    <div class="list-item">
      <img src="../assets/item.jpg" alt="" class="list-image" />
      <div class="list-title">{{ product.name }}</div>
      <div class="list-desc">
        <p class="sale-price">{{ product.salePrice }} VNĐ</p>
        <p class="price">{{ product.price }}</p>
      </div>
    </div>
  </div> -->
  <div class="list-item">
    <img src="../assets/item.jpg" alt="" class="list-image" />
    <div class="list-title">{{ product.name }}</div>
    <div class="list-desc">
      <p class="sale-price">{{ product.salePrice }}VNĐ</p>
      <p class="price">{{ product.price }} VNĐ</p>
    </div>
  </div>
  <!-- </router-link> -->
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
</style>