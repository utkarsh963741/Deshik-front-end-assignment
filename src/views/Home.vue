<template>
<v-app>
    <div class="container">
    
    <div class="mainBody columns ">
      <div class="side column is-one-fifths ">
        
      <Sidebar/>

      <Options v-bind:options="options"/>
        
      </div>
      <div class="contents  column is-four-fifths is-multiline">
        <Header/>
        <div id="nav">
          <router-link to="/">Home</router-link> |
          <router-link to="/about">About</router-link>
        </div>
        <div class="stuffContainer columns is-multiline"> 
         <div class="column is-full columns" style="height:350px;margin:0px;padding:0px;">
          <UserCounts class=" flex column is-half" v-bind:userCounts="userCounts"/>
          <EarningGraph class=" flex column is-one-thirds" style="height:310px" />
        </div>
          <div class=" flex column is-full columns" style="margin-left:10px;height:460px">
            <Foodmenu class="flex column is-one-thirds" style="height:470px"/>
            <CoustomerFeed class="flex column is-one-thirds" style="height:465px"/>
            <RecentActivities class="flex column is-one-thirds" style="height:465px"/>
          </div>

          
          <SocialMedia v-bind:social="social"  class="flex column is-full " style="margin-left:10px;height:150px;padding:0px;margin-top:5px;margin-bottom:10px;margin-left:10px;"/>

          <div class=" flex column is-full columns" style="margin-left:10px">
            <TodoList class="flex column is-one-thirds"/>
            <RecievedOrder class="flex column is-one-thirds"/>
          </div>

          <div class=" flex column is-full columns" style="margin:10px 10px; height:400px">
            <Weather class="flex column is-one-thirds"/>
            <Calender class="flex column is-one-thirds" style="padding:0px"/>
            <CurrentProgress class="flex column is-one-thirds" style="margin-bottom:0px;height:100%"/>
          </div>

          <div class="column is-full">
          <Footer/>
        </div>
        
       </div>
    </div>
      
    
    
    </div>
    
    </div>
</v-app> 
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Sidebar from '@/components/Sidebar.vue'
import Options from '@/components/Options.vue'
import UserCounts from '@/components/UserCounts.vue'
import EarningGraph from '@/components/EarningGraph.vue'
import Foodmenu from '@/components/FoodMenu.vue'
import CoustomerFeed from '@/components/CoustomerFeed.vue'
import RecentActivities from '@/components/RecentActivities.vue'
import SocialMedia from '@/components/SocialMedia.vue'
import TodoList from '@/components/TodoList.vue'
import RecievedOrder from '@/components/RecievedOrder.vue'
import Calender from '@/components/Calender.vue'
import Weather from '@/components/Weather.vue'
import CurrentProgress from '@/components/CurrentProgress.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Sidebar,
    Options,
    UserCounts,
    EarningGraph,
    Foodmenu,
    CoustomerFeed,
    RecentActivities,
    SocialMedia,
    TodoList,
    RecievedOrder,
    Calender,
    Weather,
    CurrentProgress,
    Footer
  },

  data(){
    return{
      options:[
        {id:1,name:'Dashboard',icon:'fa fa-adjust'},
        {id:2,name:'Products',icon:'fa fa-th'},
        {id:3,name:'Favourite',icon:'fa fa-star'},
        {id:4,name:'Order List',icon:'fa fa-list'},
        {id:5,name:'Booking System',icon:'fa fa-bookmark'},
        {id:6,name:'Upload Menu',icon:'fa fa-upload'},
        {id:7,name:'Charts',icon:' fa fa-signal'},
        {id:8,name:'Calender',icon:'fa fa-table'},
        {id:9,name:'UI Elements',icon:'fa fa-desktop'},
        {id:10,name:'Forms',icon:'fa fa-align-justify'},
        {id:11,name:'Data',icon:'fa fa-database'},
        {id:12,name:'E-mail',icon:'fa fa-at'},
        {id:13,name:'Profile',icon:'fa fa-cogs'},
        {id:14,name:'Map',icon:'fa fa-map-marker'},
        {id:15,name:'Login',icon:'fa fa-lock'},
      ],
      userCounts:[
        {id:1,name:'Weekly New Menu\'s',value:'1,100',icon:'fa fa-gear',color:"background:#656A85"},
        {id:2,name:'Last Week\'s Users',value:'2,900',icon:'fa fa-user',color:"background:#8E24AA"},
        {id:3,name:'Today\'s Total Earning',value:'1,999',icon:'fa fa-dollar',color:"background:#FDCD08"},
        {id:4,name:'Total Orders Recieved',value:'789',icon:'fa fa-shopping-cart',color:"background:#EE0D0D"},
      ],
      social:[
        {id:1,name:'Like us',site:'on Facebook',value:'30,000',icon:'fa fa-facebook',color:"background:#4267B2"},
        {id:2,name:'Follow us',site:'on Twitter',value:'15,000',icon:'fa fa-twitter',color:"background:#1DA1F2"},
        {id:3,name:'Follow us',site:'on Google Plus',value:'8,000',icon:'fa fa-google-plus',color:"background:#d34836"},
        {id:4,name:'Follow us',site:'on Linkedin',value:'3,500',icon:'fa fa-linkedin',color:"background:#2867B2"},
      ]
    }
  }
}
</script>

<style  scoped>

#nav{
  top:20px;
}
#nav a.router-link-exact-active {
  color: #a9a9a9;
}


.container{
   font-family:'Roboto Mono',sans-serif,monospace;
  width:100%;
  flex-direction: row;
  left: 0px;
  margin:0 0 0 0;
  padding:0px;
  height:100%
}



.mainBody{
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap:nowrap;
  align-items:top;  
  justify-content:flex-start;
  padding:0px;
  margin: 0px;
}
.side{
  display: flex;
  flex-direction: column;
  min-width: 200px;
  height: auto;
  padding:0px;
  
}
.contents{
  display: flex;
  min-width: 1065px;
  flex-direction: column;
  height:1950px;
  background-color:#e3e3e3;
  margin: 0 0 0 0;
  padding: 0 0 0 0;
  width:97%
}

.stuffContainer{
  margin-left: 20px;
  margin-right: 20px;
  height:3000px
}

.flex{
  margin-right: 10px;
  margin-bottom: 20px;
  height:350px;
}
</style>
