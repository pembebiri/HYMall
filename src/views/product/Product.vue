<template>
  <div class="product">
    <ImageView></ImageView>
   <Content></Content>
  </div>
</template>

<script>

import Content from './childComps/Content'
import ImageView from './childComps/ImageView'

export default{
  name:"Product",
  components:{
     Content,
     ImageView
  }
}
</script>

<style>
.product{
 display: flex;
}
</style>