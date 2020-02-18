<template>
<div class="container">
 <template>
  <v-card
    class="mt-4 mx-auto"
    max-width="600"
    height="300px"
  >
    <v-sheet
      class="v-sheet--offset mx-auto"
      color="cyan"
      elevation="12"
      max-width="calc(100% - 32px)"
      height="220px"
    >
      <v-sparkline
        :labels="labels"
        :value="value"
        color="white"
        line-width="2"
        padding="16"
        height="120px"
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <div class="title font-weight-light mb-2">Earning Graph</div>
      
      <v-divider class="my-2"></v-divider>
      <v-icon
        class="mr-2"
        small
      >
        mdi-clock
      </v-icon>
      <span class="caption grey--text font-weight-light">last registration 26 minutes ago</span>
    </v-card-text>
  </v-card>
</template>
 
</div>
  
</template>

<script>
  export default {
    data: () => ({
      labels: [
        'Q4 2017',
        'Q1 2018',
        'Q2 2018',
        'Q3 2018',
        'Q4 2018',
        'Q1 2019',
        'Q2 2019',
        'Q3 2019',
      ],
      value: [
        200,
        175,
        420,
        390,
        290,
        410,
        500,
        415,
      ],
    }),
  }
</script>

<style scoped>
  .container{
    height: 100px;
  }

  .v-sheet--offset {
    top: -24px;
    position: relative;
  }
</style>