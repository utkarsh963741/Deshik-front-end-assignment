<template>
<div class="container">
<v-card
    max-width="455"
    class="mx-auto"
  >
    <v-toolbar color="white" dark  style="height:60px">
      
      <v-toolbar-title style="color:black">Current Progress</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon color="black">mdi-dots-horizontal</v-icon>
      </v-btn>
    </v-toolbar>
  <div v-for="ex in ex" :key="ex.id" style="margin:10px">
    <v-slider
      v-model="ex.val"
      :color="ex.color"
      :label="ex.label"
    ></v-slider>

  </div> 
</v-card>
</div>
</template>


<script>
  export default {
    data () {
      return {
        ex:[
          {id:1,val:30,color:'orange darken-3', label:'Bootstrap'},
          {id:2,val:82,color:'green darken-3', label:'Vue'},
          {id:3,val:40,color:'black darken-3', label:'Unity'},
          {id:4,val:20,color:'blue darken-3', label:'Flutter'},
          {id:5,val:55,color:'red darken-3', label:'NMap'},
        ]}}


  }
</script>





<style scoped>
.container{
    background-color: #e3e3e3;
    height: 250px;
    overflow:hidden;
    width: max-content
  }



</style>