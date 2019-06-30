<template>
  <v-card color="grey">
    <v-card-title class="headline white--text">knowledge</v-card-title>
    <v-card-text>
      <pie-chart
        :chart-data="chartData"
        :options="chartOptions"
        :height="300"
      />
    </v-card-text>
  </v-card>
</template>

<script>
import colors from 'vuetify/es5/util/colors'

export default {
  data() {
    return {
      chartDataValues: [],
      chartColors: [
        colors.red.lighten1,
        colors.blue.lighten1,
        colors.yellow.lighten1,
        colors.green.lighten1
      ],
      chartLabels: ['Programing', 'Financial', 'Accounting', 'Mathematics'],
      chartOptions: {
        maintainAspectRatio: false,
        animation: {
          duration: 500,
          easing: 'easeInOutCubic'
        },
        legend: {
          labels: {
            fontColor: 'white'
          }
        }
      }
    }
  },
  computed: {
    chartData() {
      return {
        datasets: [
          {
            data: this.chartDataValues,
            backgroundColor: this.chartColors
          }
        ],
        labels: this.chartLabels
      }
    }
  },
  mounted: function() {
    this.initalize()
  },
  methods: {
    initalize() {
      const data = [50, 25, 20, 5]
      this.chartDataValues = data
    }
  }
}
</script>

<style></style>
