<template>
  <div class="content">
    <div class="name">{{ name }}</div>
    <div class="price">{{ price }}</div>
    <div class="button">Add to Cart</div>
  </div>
</template>

<script>
export default{
 name:'Content',
 props:{
    name:String,
    price:String
 }
}
</script>

<style scoped>
.content{
    background-color: white;
    padding:100px;
    padding-left: 100px;
}
.name{
  width: 100%;
  height: 20px;
  font-size: large;
  text-align: left;
  color:black;
}
.price{
 width: 100%;
 height: 20px;
 margin:5px;
 font-size: small;
 color: gray;
 text-align: left;
}
.price:disabled{
    text-decoration: line-through;
}
.button{
  padding: 5px;
  border-radius: 8px;
  border-style: solid;
  background-color: #ff8198;
  border-color: #ff8198;
  color: white;
  font-family:'Source Sans 3';
  text-align: center;
}
.button:hover{
 background-color: white;
  border-color: #ff8198;
  border-style: solid; 
  border-radius: 8px;
  color: #ff8198;
}
</style>