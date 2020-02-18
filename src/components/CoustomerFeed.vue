<template>
  <div class="container">
  <v-card
    max-width="455"
    class="mx-auto"
  >
    <v-toolbar color="white" dark  style="height:60px">
      
      <v-toolbar-title style="color:black">Coustomer Feed</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon color="black">mdi-dots-horizontal</v-icon>
      </v-btn>
    </v-toolbar>

    <v-list three-line >
      
        <v-list-item  v-for="(item) in items" :key="item.title" style="height:60px">
          <v-list-item-avatar>
            <v-img :src="item.avatar"></v-img>
          </v-list-item-avatar>

          <v-list-item-content style="padding:0px;height:60px" >
            <v-list-item-title v-html="item.title" style="font-size:15px;margin:0px"></v-list-item-title>
            <v-list-item-subtitle v-html="item.subtitle" style="font-size:10px"></v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      
    </v-list>
  </v-card>
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          title: "<span class='text--primary'>Ali Connors</span>",
          subtitle: " &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?",
        },
      
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
          title: '<span class="text--primary">to Alex, Scott, Jennifer</span> <span class="grey--text text--lighten-1">4</span>',
          subtitle: " &mdash; Wish I could come, but I'm out of town this weekend.",
        },
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
          title: 'Oui oui',
          subtitle: "&mdash; Do you have Paris recommendations? Have you ever been?",
        },
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/4.jpg',
          title: '<span class="text--primary">Trevor Hansen</span>',
          subtitle: " &mdash; Have any ideas about what we should get Heidi for her birthday?",
        },
        {
          avatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg',
          title: 'Recipe to try',
          subtitle: "<span class='text--primary'>Britta Holt</span> &mdash; We should eat this: Grate, Squash, Corn, and tomatillo Tacos.",
        },
      ],
    }),
  }
</script>

<style scoped>
.container{
    background-color: #e3e3e3;
    height: 200px;
    overflow:scroll;
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch;
    
    width: max-content
  }

::-webkit-scrollbar{
  width: 5px;
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
    
    background-color: #F5F5F5;
    border-radius: 10px;
    width: 4px;
    
  
}

</style>