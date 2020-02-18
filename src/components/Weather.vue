<template>
<div class="container">
 
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <div style="background: #2867B2;padding:10px">
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title class="headline" style="color:white">San Francisco</v-list-item-title>
        <v-list-item-subtitle style="color:white">Mon, 12:30 PM, Mostly sunny</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-card-text>
      <v-row align="center" style="height:30px">
        <v-col class="display-1" cols="6" style="color:white" >
          23&deg;C
        </v-col>
        <v-col cols="6" >
          <v-icon large=""  style="color:white" >
        mdi-white-balance-sunny
      </v-icon>
        </v-col>
      </v-row>
    </v-card-text>
    </div>

    <v-slider
      v-model="time"
      :max="6"
      :tick-labels="labels"
      class="mx-4"
      ticks
    ></v-slider>

    
      <v-row v-for="item in forecast"
        :key="item.day" align="center">
        <v-col> {{ item.day }}</v-col>
        <v-col>
         
            <v-icon>{{ item.icon }}</v-icon>
          
        </v-col>
        <v-col>
          <v-list-item-subtitle class="text-right">
            {{ item.temp }}
          </v-list-item-subtitle>
        </v-col>
      </v-row>
      

    <v-divider></v-divider>

    
  </v-card>

 
</div>
  
</template>

<script>
  export default {
    data () {
      return {
        labels: ['SU', 'MO', 'TU', 'WED', 'TH', 'FR', 'SA'],
        time: 0,
        forecast: [
          { day: 'Tuesday', icon: 'mdi-white-balance-sunny', temp: '24\xB0/12\xB0' },
          { day: 'Wednesday', icon: 'mdi-white-balance-sunny', temp: '22\xB0/14\xB0' },
          { day: 'Thursday', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
        ],
      }
    },
  }
</script>

<style scoped>
  .container{
    background-color: aquamarine;
    height: 100px;
  }
</style>