<template>
  <div class="container">
  
  <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"
  >

  <template v-slot:top>
      <v-toolbar flat color="white">
        <v-toolbar-title>Recieved Orders</v-toolbar-title>
        <v-divider
          class="mx-4"
          inset
          vertical
        ></v-divider>
        <v-spacer></v-spacer>
        <v-dialog v-model="dialog" max-width="500px">
          <template v-slot:activator="{ on }">
            <v-btn color="primary" dark class="mb-2" v-on="on">New Item</v-btn>
          </template>
          
        </v-dialog>
      </v-toolbar>
    </template>
    <template v-slot:item.calories="{ item }"  >
      <v-chip :color="getColor(item.calories)" dark style="margin:7px" >{{ item.calories }}</v-chip>
    </template>
  </v-data-table>

  </div>
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'Coustomer',
            align: 'left',
            sortable: false,
            value: 'name',
          },
          
          { text: 'Order ID', value: 'fat' },
          { text: 'Products', value: 'carbs' },
          { text: 'Quantity', value: 'protein' },
          { text: 'Status', value: 'calories' },
          
        ],
        desserts: [
          {
            name: 'Steve Jobs',
            calories: 'Paid',
            fat: '#72683',
            carbs: 'Pizza',
            protein: 10,
            iron: '1%',
          },
          {
            name: 'Elon Musk',
            calories:'Pending' ,
            fat:'#674764' ,
            carbs: 'Burger',
            protein: 12,
            iron: '1%',
          },
        
          {
            name: 'Varun Dhavan',
            calories: 'Pending',
            fat: '#312332',
            carbs: 'Cold Drinks',
            protein: 8,
            iron: '2%',
          },
          {
            name: 'Leonardo De Caprio',
            calories: 'Failed',
            fat: '#092301',
            carbs: 'Pasta',
            protein: 7,
            iron: '45%',
          },
         
        ],
      }
    },
    methods: {
      getColor (calories) {
        if (calories =='Failed') return 'red'
        else if (calories =='Pending') return 'orange'
        else return 'green'
      },
    },
  }
</script>

<style scoped>
  .container{
    background-color: aquamarine;
    height: 400px;
  }
</style>