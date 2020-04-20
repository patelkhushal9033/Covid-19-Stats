<template>
    <div class="text-center subtitle-2">Pie Chart<apexchart class="my-6" type="donut" height="300" width="100%" :options="chartOptions" :series="donutSeries"></apexchart></div>
</template>

<script>
import VueApexCharts from 'vue-apexcharts'

export default {
    components: {
        apexchart: VueApexCharts
    },
    data () {
        return {
            chartOptions: {
                plotOptions: {
                    pie: {
                        donut: {
                            labels: {
                                show: true,
                            }
                        }
                    }
                },
                legend: {
                    position: 'bottom'
                },
                colors: ['#b33939', '#218c74', '#cd6133', '#cc8e35'],
                labels: ["Deaths", "Recovered", "Active", "Critical"],
            },
            donutSeries: [12045, 80938, 82903, 8930],
        }
    }
}
</script>