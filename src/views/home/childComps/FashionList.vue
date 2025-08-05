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
  padding-bottom: 75px;
}
.fashion-list:hover{
  background-color: #ff8198;
}

.box {
  background-color: white;
  padding: 0.5rem;
  text-align: center;
  width: 200px;
  margin: 20px;
}

.image {
  width: 100%;
  height: 100%;
}

.product-name {
  font-family: 'Times New Roman', Times, serif;
  font-size: large;
  margin-top: 0.5rem;
  text-align: left;
}

.product-price {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande',
    'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: smaller;
  font-style: italic;
  margin-top: 0.3rem;
  text-align: left;
}

.product-price.passive {
  text-decoration: line-through;
  color: gray;
  opacity: 0.6;
  text-align: left;
}
</style>