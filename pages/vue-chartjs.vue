<template>
  <div>
    <h1>vue-chartjsで棒グラフ</h1>
    <BarChart :chartdata="chartdata" :options="options" />
  </div>
</template>

<script>
import BarChart from '@/components/BarChart.vue'

export default {
  components: {
    BarChart
  },
  data () {
    return {
      chartdata: {
        labels: ['January', 'February'],
        datasets: [
          {
            label: ['Data One'],
            backgroundColor: '#f87979',
            data: [40, 30]
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  }
}
</script>
