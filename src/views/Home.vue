<template>
  <div class="home">
    <div class="container">
    
    <div class="mainBody">
      <div class="side">
        
      <Sidebar/>
        
        
      <Options v-bind:options="options"/>
        
      </div>
      <div class="contents">
        <Header/>
        <p>axZCcxcXc</p>
        <p>hsadbjhdbvshdb</p>
       </div>
    </div>
      
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Header from '@/components/Header.vue'
import Sidebar from '@/components/Sidebar.vue'
import Options from '@/components/Options.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Header,
    Sidebar,
    Options
  },

  data(){
    return{
      options:[
        {id:1,
        name:'Dashboard',
        icon:'fa fa-adjust'},
        
        {id:2,
        name:'Products',
        icon:'fa fa-th'},

        {id:3,
        name:'Favourite',
        icon:'fa fa-star'},

        {id:4,
        name:'Order List',
        icon:'fa fa-list'},

        {id:5,
        name:'Booking System',
        icon:'fa fa-bookmark'},

        {id:6,
        name:'Upload Menu',
        icon:'fa fa-upload'},

        {id:7,
        name:'Charts',
        icon:' fa fa-signal'},

        {id:8,
        name:'Calender',
        icon:'fa fa-table'},

        {id:9,
        name:'UI Elements',
        icon:'fa fa-desktop'},

        {id:10,
        name:'Forms',
        icon:'fa fa-align-justify'},

        {id:11,
        name:'Data',
        icon:'fa fa-database'},

        {id:12,
        name:'E-mail',
        icon:'fa fa-at'},

        {id:13,
        name:'Profile',
        icon:'fa fa-cogs'},

        {id:14,
        name:'Map',
        icon:'fa fa-map-marker'},

        {id:15,
        name:'Login',
        icon:'fa fa-lock'},
      ]
    }
  }
}
</script>

<style>
.home{
  font-family:'Roboto Mono',sans-serif,monospace;
}
.container{
  display: inline-block;
  width: 100%;
  flex-direction: row;
  align-items: top;
  justify-content: center;
}



.mainBody{
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap:nowrap;
  align-items:top;  
  justify-content:flex-start;
  

}
.side{
  display: flex;
  flex-direction: column;
  width: 18%;
  min-width: 200px;
  height: auto;
  
  
}
.contents{
  display: flex;
  min-width: 1065px;
  flex-direction: column;
 
  width:82%;
  height: 700px;
  background-color:#e3e3e3;
}

.flex{
  display: flex;
}
</style>
