<template>
  <div class="content">
    <div class="name">
      <slot class="name"> Birinci  </slot>
    </div>
    <div>
      <slot class="price"> 35 lira    </slot>
    </div>
    <div class="button"> 
        <slot> Add to Cart </slot>
    </div>
  </div>
</template>

<script>
export default{

}
</script>
<style>
.content{
    background-color: white;
    padding:100px;
    padding-left: 150px;
}
.name{
  width: 100%;
  height: 20px;
  padding:30px;
  font-size: large;
  text-align: left;
  color:black;
}
.price{
 width: 100%;
 height: 20px;
 margin:50px;
 font-size: small;
 color: gray;
 text-align: left;
}
.price:disabled{
    text-decoration: line-through;
}
.button{
  margin: 15px;
  padding: 5px;
  border-radius: 8px;
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