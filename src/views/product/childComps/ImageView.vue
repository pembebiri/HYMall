<template>
  <div class="image-container">
    <img :src="src" alt="Product Image" />
  </div>
</template>

<script>
export default {
   name: 'ImageView',
    props: {
        src: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
.image-container {
  width: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; 
}

.image-container img {
  width: 100%;
  height: auto;
  object-fit: cover; }
</style>