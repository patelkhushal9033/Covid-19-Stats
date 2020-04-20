<template>
  <v-app>
    <v-content>
      <v-container
        ma-0
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
