<template>
  <v-app class="appContainer">
    <v-content>
      <v-container
        pa-0>
        <v-app-bar 
          flat
          dense
          color="#FCFBFE">
          <v-spacer/>
          <span class="subtitle-2">{{title}}</span>
          <v-spacer/>
        </v-app-bar>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: 'Covid 19 - We Are All In This Together'
    }
  }
}
</script>

<style scoped>

.appContainer {
  margin-left: auto !important;
  margin-right: auto !important;
}

</style>
