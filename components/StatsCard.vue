<template>
    <v-flex>
        <div 
          class="statsCard"
          style="display: flex; overflow-x: auto">
          <v-card 
            class="moreInfo white--text" color="#b33939">
            <div class="text-center body-2">Deaths</div>
            <div class="text-center headline">12045</div>
            <div class="text-center caption">+ 321 today</div>
          </v-card>
          <v-card 
            class="moreInfo white--text" color="#218c74">
            <div class="text-center body-2 mb-2">Recovered</div>
            <div class="text-center headline">80567</div>
          </v-card>
          <v-card 
            class="moreInfo white--text" color="#cd6133">
            <div class="text-center body-2 mb-2">Active</div>
            <div class="text-center headline">80787</div>
          </v-card>
          <v-card 
            class="moreInfo white--text" color="#cc8e35">
            <div class="text-center body-2 mb-2">Critical</div>
            <div class="text-center headline">5678</div>
          </v-card>
        </div>
    </v-flex>
</template>


<script>
export default {
    
}
</script>

<style scoped>

.moreInfo {
  padding: 2%;
  margin-right: 5%;
  min-width: 43%;
  background-color: #cc8e35;
  border-radius: 12px !important;
  color: white;
}

.statsCard::-webkit-scrollbar {
  display: none;
}

</style>