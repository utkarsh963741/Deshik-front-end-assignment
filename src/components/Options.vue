<template>
  <div>
    <div class="optionContainer">
        <div >
          <ul class="list" v-for="options in options" :key="options.id">
            <li class="options"><i :class="options.icon"></i><a href="">{{options.name}}</a></li>
          </ul>

        </div>
    </div>

  </div>
  
</template>

<script>
export default {
  name:'options',

  props:{
    options:Array,
  },

  
  
  
}
</script>

<style  scoped>
.optinContainer{
  display: flex;
  flex-direction: row;
  background-color: #f9f9f9;
}
.list{
  margin: 0;
  padding: 0;
  align-items: center;
  justify-content: space-between;
}

ul li{
  height: 40px;
  display: flex;
  list-style: none;
  color: #a9a9a9;
  width: 100%;
  align-items: center;
  padding-left: 20px;
  margin:0;
  border:0;
}
ul li:hover{
  background-color: #e9e9e9;
  color: red;
  text-decoration-color: gray;
  font-size: 1.05em;
}
ul li a{
  display: flex;
  text-decoration: none;
  color:#a9a9a9; 
  font-size: 15px;
}
ul li i{
  margin-right: 25px
}

</style>