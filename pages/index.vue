<template>
  <v-layout>
    <v-container pa-0>
      <v-col
        class="infoBlocks totalNumber">
        <div class="caption text-center ">World</div>
        <div class="display-1 text-center">15203089</div>
        <div class="caption text-center">+ 1237 (2.32%) <span>today</span></div>
      </v-col>
      <v-col class="infoBlocks">
        <StatsCard/>
      </v-col>
      <v-col class="infoBlocks"> 
        <LineChart/>
      </v-col>
      <v-col> 
        <PieChart/>
      </v-col>
      <v-col class="infoBlocks"> 
        <DataTable/>
      </v-col>
    </v-container>
  </v-layout>
</template>

<script>
import LineChart from '~/components/LineChart.vue'
import PieChart from '~/components/PieChart.vue'
import StatsCard from '~/components/StatsCard.vue'
import DataTable from '~/components/DataTable.vue'

export default {
  components: {
    LineChart,
    PieChart,
    StatsCard,
    DataTable
  },
  data() {
    return {
    }
  }
}
</script>

<style scoped>
.infoBlocks {
  margin-bottom: 5%;
}

.totalNumber {
  margin-top: 5%;
}

</style>

