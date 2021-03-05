<template>
  <div>
    <h1>vue-chartjsで棒グラフ</h1>
    <BarChart :chartdata="chartdata" :options="options" />
  </div>
</template>

<script>
// import BarChart from '@/components/BarChart.vue'
import Data from '@/data/bar.json'

export default {
  // components: {
  //  BarChart
  // },
  data () {
    return {
      chartdata: {
        labels: Data.data.map(data => data.month),
        datasets: [
          {
            label: ['Data One'],
            backgroundColor: '#f87979',
            data: Data.data.map(data => data.sale)
          }
        ]
      }
    }
  }
}
</script>
