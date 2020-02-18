<template>
  <div class="container">
  <v-card
    max-width="450"
    class="mx-auto"
  >
    <v-toolbar color="white"  dark>
      <v-toolbar-title style="color:black">Hot Food Menu</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon color="black">mdi-dots-horizontal</v-icon>
      </v-btn>
    </v-toolbar>

    <v-list>
      <v-list-group v-for="item in items" :key="item.title" no-action >
        
        <template v-slot:activator style="height:30px">
         
          
          
          <p style="font-size:20px">   |    </p>
          <v-list-item-content style="margin:0px;padding-top:14px;padding-bottom:16.5px" >
            <v-list-item-title  v-text="item.title" style="font-size:20px;"></v-list-item-title>
            
          </v-list-item-content>
          <p style="color:red;font-size:15px;margin-top:10px">{{item.price}}</p>
          
        </template>

        <v-list-item
          v-for="subItem in item.items"
          :key="subItem.title"
        >
          <v-list-item-content>
            <v-list-item-title v-text="subItem.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
  </v-card>

  </div>
</template>


<script>
  export default {
    data () {
      return {
        items: [
          {
            price:'Rs. 100',
            title: 'Burger',
            avatar: 'fa fa-cheeseburger',
            items: [
              { title: 'List Item' },
            ],
          },
          {
            price:'Rs. 300',
            title: 'Pizza',
            active: true,
            avatar: 'fa fa-pizza',
            items: [
              { title: 'Panner    Rs.350' },
              { title: 'Mushroom     Rs.400' },
              { title: 'Chicken Sausage     Rs.500' },
            ],
          },
          {
            price:'Rs. 150',
            title: 'Pasta',
            avatar: '../assets/pasta.jpg',
            items: [
              { title: 'List Item' },
            ],
          },
          {
            price:'Rs. 50',
            title: 'Cold-Drinks',
            avatar: '../assets/colddrink.jpg',
            items: [
              { title: 'Pepsi     Rs.40' },
              { title: 'Coca-Cola    Rs.40' },
              { title: 'Mountain Dew     rs.40' },
            ],
          },
          {
            price:'Rs. 250',
            title: 'Dessert',
            avatar: '../assets/desert.jpg',
            items: [
              { title: 'List Item' },
            ],
          },

          {
            price:'Rs. 20',
            title: 'Samosa',
            avatar: '../assets/pasta.jpg',
            items: [
              { title: 'List Item' },
            ],
          },
          {
            price:'Rs. 199',
            title: 'Biryani',
            avatar: '../assets/pasta.jpg',
            items: [
              { title: 'List Item' },
            ],
          },
        
        ],
      }
    },
  }
</script>


<style scoped>
  .container{
    background-color: #e3e3e3;
    height: 450px;
    overflow:scroll;
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch;
    
    width: max-content;
    
  }

  ::-webkit-scrollbar{
  width: 4px;
}

::-webkit-scrollbar-thumb{
 border-radius: 10px;
 width: 7px;
    background-image: -webkit-gradient(linear,
                                       left bottom,
                                       left top,
                                       color-stop(0.44, rgb(122,153,217)),
                                       color-stop(0.72, rgb(73,125,189)),
                                       color-stop(0.86, rgb(28,58,148)));
}
.container::-webkit-scrollbar-track{
    
    background-color: #e3e3e3;
    border-radius: 10px;
    width: 4px;
  
}
</style>