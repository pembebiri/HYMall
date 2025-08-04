<template>
  <div class="fashion-list">
    <div class="box" v-for="(item, index) in items" :key="index">
      <img :src="item.img" alt="" class="image" />

      <div class="product-name">{{ item.title }}</div>

      <div :class="['product-price', { passive: isPassive }]">
        {{ item.price || '₺35' }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FashionList',
  props: {
    items: {
      type: Array,
      required: true
    },
    isPassive: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.fashion-list {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
  padding: 1rem;
}

.box {
  background-color: white;
  padding: 1rem;
  text-align: center;
  border-radius: 8px;
  width: 200px;
  
}
.box:hover{
  background-color: #ff8198;
}
.image {
  width: 100%;
  height: 100%;
  border-radius: 6px;
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
