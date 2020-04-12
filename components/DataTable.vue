<template>
    <v-flex>
     <div class="subtitle-1 font-weight-medium mb-7">Entire World</div>
     <v-data-table
        :headers="headers"
        :items="tableData"
        class="elevation-1">
     </v-data-table>
    </v-flex>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            headers: [
                {text: 'Country', align: 'start', value: 'country'},
                {text: 'Cases', value: 'cases'},
                //{text: 'Today Cases', value: 'todayCases'},
                {text: 'Deaths',  value: 'deaths'},
                //{text: 'Today Deaths', value: 'todayDeaths'},
                {text: 'Recovered', value: 'recovered'},
                {text: 'Active', value: 'active'},
                //{text: 'Critical', value: 'critical'}
            ],
            tableData: [
                {
                    country: 'demo',
                    cases: '123',
                    todayCases: '23',
                    deaths: '13',
                    todayDeaths: '3',
                    recovered: '45',
                    active: '56',
                    critical: '32'
                }
            ]
        }
    },
    mounted() {
        axios.get("https://coronavirus-19-api.herokuapp.com/countries").then(Response => {this.tableData = Response.data})
  }
}
</script>

