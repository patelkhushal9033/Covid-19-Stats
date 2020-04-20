<template>
    <div class="chart text-center subtitle-2">Area Chart<apexchart type="area" height="300" width="100%" :options="options" :series="series"></apexchart></div>
</template>


<script>
import VueApexCharts from 'vue-apexcharts'


export default {
    components: {
        apexchart: VueApexCharts
    },
    data() {
        return {
            options: {
                chart: {
                    toolbar: {
                        show: false,
                    },
                },
                
                dataLabels: {
                    enabled: false
                },
            
                stroke: {
                    curve: 'smooth'
                },

                colors: ['#b33939', '#218c74', '#2c2c54'],
            
                xaxis: {
                    categories: ["02 Mar", "03 Mar", "04 Mar", "05 Mar", "06 Mar", "07 Mar", "08 Mar", "09 Mar", "10 Mar", "11 Mar", "12 Mar", "13 Mar", "14 Mar"]
                },
            
                tooltip: {
                    x: {
                        format: 'dd/MM/yy HH:mm'
                     },
                },
            },
            series: [{
                name: 'Death',
                data: [1289, 1080, 6173, 1739, 8918, 1848, 3671, 3101, 1448, 1891, 2451, 548, 1921]
            }, 
            {
                name: 'Recovery',
                data: [89, 100, 673, 39, 18, 848, 671, 301, 1048, 891, 251, 548, 921]
            },
            {
                name: 'New Cases',
                data: [3011, 3078, 6910, 5639, 4301, 8048, 8921, 6301, 10048, 8921, 2351, 5048, 4921]
            }],
            
        }
        
    }
    
}
</script>
