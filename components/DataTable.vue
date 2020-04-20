<template>
    <v-flex>
        <div class="text-center subtitle-2 mb-8">Entire World</div>
        <v-flex row class="header">
            <v-card
                flat
                class="moreInfo country" width="25%">
                <div class="text-left font-weight-bold">Country</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo case" width="20%">
                <div class="text-right font-weight-bold">C</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo death" width="17%">
                <div class="text-right font-weight-bold">D</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo recovered" width="19%">
                <div class="text-right font-weight-bold">R</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo active" width="19%">
                <div class="text-right font-weight-bold">A</div>
            </v-card>
        </v-flex>
        <v-flex class="sty"
            v-for="tableData in tableData"
            :key="tableData.country"
            row>
            <v-card
                flat
                class="moreInfo" width="25%">
                <div class="text-left">{{tableData.country}}</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo" width="20%">
                <div class="text-right">{{ tableData.cases }}</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo" width="17%">
                <div class="text-right">{{ tableData.deaths }}</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo" width="19%">
                <div class="text-right">{{ tableData.recovered }}</div>
            </v-card>
            <v-card 
                flat
                class="moreInfo" width="19%">
                <div class="text-right">{{tableData.active }}</div>
            </v-card>
        </v-flex>
    </v-flex>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            tableData: [
                {
                    country: '',
                    cases: '',
                    todayCases: '',
                    deaths: '',
                    todayDeaths: '',
                    recovered: '',
                    active: '',
                    critical: ''
                }
            ]
        }
    },
    mounted() {
        axios.get("https://coronavirus-19-api.herokuapp.com/countries").then(Response => {this.tableData = Response.data})
  }
}
</script>

<style scoped>
.moreInfo {
  padding: 2%;
  border-radius: 0 !important;
  background-color: #F5F7FB;
  border-bottom: #E6E6F6 1px solid;
  color: #575757;
font-size: 12px;

}

.sty:nth-child(odd) {
    background-color: #FCFBFE;
}
.moreInfo:nth-child(even) {
    background-color: #FFFFFF;
}

.header {
  border-bottom: #E6E6F6 1.2px solid;
    
}

.row {
    margin: 0 !important
}

.country {
    color: #2c2c54;
}

.case {
    color: #474787;
}

.death {
    color: #b33939;
}

.recovered {
    color:#218c74;
}

.active {
    color: #cd6133;
}

@media only screen and (min-width: 600px) {
  .moreInfo {
    font-size: 14px;
  }
}
</style>

