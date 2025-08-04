<template>
  <div class="box">
     <slot name="image" />

    <div class="product-name">
      <slot name="product-name">Etek</slot>
    </div>

    <div :class="['product-price', { passive: isPassive }]">
      <slot name="product-price">₺35</slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FashionList',
  props: {
    isPassive: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.box {
  background-color: antiquewhite;
  padding: 1rem;
  text-align: center;
  border-radius: 8px;
  width: 200px;
}

.product-name {
  font-family: 'Times New Roman', Times, serif;
  font-size: large;
  margin-top: 0.5rem;
}

.product-price {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande',
    'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: smaller;
  font-style: italic;
  margin-top: 0.3rem;
}

.product-price.passive {
  text-decoration: line-through;
  color: gray;
  opacity: 0.6;
}
</style>