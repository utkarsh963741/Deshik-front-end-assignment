<template>
  <v-card height="100" width="2700px">
    <v-footer
      absolute
      class="font-weight-medium"
      style="background:#e3e3e3"
    >
      <v-col
        class="text-center"
        cols="12" style="background:#e3e3e3"
      >
        {{ new Date().getFullYear()+'-'+new Date().getMonth()+'-'+new Date().getDate()+'  '+new Date().getHours()+':'+new Date().getMinutes()+':'+new Date().getSeconds() }}
         @
        <strong>Utkarsh Singh</strong>
      </v-col>
    </v-footer>
  </v-card>
</template>