<template>
  <div class="shop-item">
    <h3>{{ title }}</h3>
    <img src="../../assets/iphone.jpeg" width="100" height="100" />
    <p>Shop new from $ {{ newPrice }}</p>
    <p>Shop used from $ {{ usedPrice }}</p>
  </div>
</template>

<script>
export default {
  props: ["imgSrc", "newPrice", "usedPrice", "title"],
  created() {
    console.log(this.imgSrc);
  },
  computed: {
    imgLink() {
      console.log("../../assets/" + this.imgSrc);
      return "../../assets/" + this.imgSrc;
    },
  },
};
</script>

<style scoped>
.shop-item {
  display: inline-block;
  text-align: center;
  border: 1px solid brown;
  border-radius: 25px;
  height: 250px;
  margin: 50px;
  width: 200px;
}

.shop-item:hover {
  cursor: pointer;
  height: 300px;
  width: 300px;
  font-size: 22px;
}

.shop-item img {
  padding-left: 20px;
}
</style>
