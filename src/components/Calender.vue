<template>
<div>
  <v-row justify="center" style="margin:0px 10px">
    <v-date-picker v-model="picker"></v-date-picker>
  </v-row>
  </div>
</template>


<script>
  export default {
    data () {
      return {
        picker: new Date().toISOString().substr(0, 10),
        landscape: true,
      }
    },
  }
</script>