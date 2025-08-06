<template>
  <div class="product">
    <ImageView :src="imgUrl" />
    <Content :name="productName" :price="productPrice" />
  </div>
</template>
<script>
import Content from './childComps/Content'
import ImageView from './childComps/ImageView'

export default {
  name: "Product",
  components: {
    Content,
    ImageView
  },
  data() {
    return {
      imgUrl: this.$route.query.img,
      productName: this.$route.query.name,
      productPrice: this.$route.query.price
    }
  }
}
</script>
<style scoped>
.product {
  display: flex;
  gap: 30px;
  padding: 50px;
  background-color: #f8f8f8;
}
</style>