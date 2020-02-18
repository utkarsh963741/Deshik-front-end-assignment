<template>
<div class="columns">
 <div v-for="social in social" :key="social.id" class="column " style="height:160px;" > 
   <div :style="social.color" style="border-radius:5px">
      <i style="padding:10px;transform:translateX(-100px);font-size:30px"  :class="social.icon"></i>
   <div class="flex  columns"  style="align-items:center;justify-content:flex-top;height:75px;padding-left:9px;margin:0px;">
      
      
      <div class="column rows " style="font-size:13px"><div class="row">{{social.name}}</div><div class="row">{{social.site}}</div></div>
       <div style="font-size:30px">|</div>  
      <div class="column" style="font-size:30px">{{social.value}} </div>
   </div>
  </div>
  </div>
 </div>
  
</template>

<script>
export default {
  name:'social',
  props:{
    social:Array,
  }
  
}
</script>

<style scoped>
  .flex{
    height:150px;
    width: 130;
    color:white;
    text-decoration-color: white;
  }
</style>