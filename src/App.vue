<template>
  <home-page></home-page>
  <div class="shop-items">
    <shop-item
      :imgSrc="'iphone.jpeg'"
      :newPrice="499.99"
      :usedPrice="199.99"
      :title="'iPhone 12'"
    ></shop-item>
    <shop-item
      :imgSrc="'iphone.jpeg'"
      :newPrice="499.99"
      :usedPrice="199.99"
      :title="'iPhone 12 X PRO'"
    ></shop-item>
    <shop-item
      :imgSrc="'iphone.jpeg'"
      :newPrice="499.99"
      :usedPrice="199.99"
      :title="'Samsung Galaxy X10'"
    ></shop-item>
  </div>
</template>
<script>
import HomePage from "./components/pages/HomePage.vue";
import ShopItem from "./components/UI/ShopItem.vue";

export default {
  components: {
    HomePage,
    ShopItem,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: white;
}

.shop-items {
  margin-left: 200px;
  margin-right: 200px;
}
</style>
