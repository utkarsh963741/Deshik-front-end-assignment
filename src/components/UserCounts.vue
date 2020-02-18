<template>
  <div>
    <div class="columns is-multiline" style="height:100%" >
      <div v-for="userCounts in userCounts" :key="userCounts.id" class="column is-half "  > 
          <div class="countBox  " :style="userCounts.color" style="border-radius:10px" >
            <div style="display:flex;justify-content:space-between;padding:10px 10px 0px 10px">
              <div><i :class="userCounts.icon" style="color:white;font-size:32px"></i></div>
              <div><i class="fa fa-spinner fa-pulse" style="color:white"></i></div>
            </div>
            <div class="flex" style="font-size:20px;color:white">{{userCounts.value}}</div>
            <div class="flex" style="font-size:15px;font-fanmily:sans;color:white;margin-top:10px">{{userCounts.name}}</div>
          </div>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  name:'userCounts',
  props:{
    userCounts:Array,
  }
}
</script>

<style scoped>
  

  .countBox{
    display: inline-flexbox;
    flex-direction: row;
    width: auto;
    height:125px;
    margin-left: 5px;
    padding: 2px;
  }

  
</style>