<template>
  <v-card color="grey">
    <v-card-title class="headline white--text">Learning</v-card-title>
    <v-card-text>
      <doughnut-chart
        class="chart_price"
        :chart-data="chartData"
        :options="chartOptions"
        :height="300"
      ></doughnut-chart>
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
        colors.yellow.lighten1,
        colors.green.lighten1,
        colors.purple.lighten1,
        colors.green.darken2,
        colors.indigo.darken2,
        colors.orange.darken1,
        colors.blue.darken1
      ],
      chartLabels: [
        'Python',
        'Javascript',
        'PHP',
        'nginx',
        'mariadb',
        'postgreSQL',
        'Docker'
      ],
      chartOptions: {
        cutoutPercentage: 20,
        maintainAspectRatio: false,
        animation: {
          duration: 4000,
          steps: 100,
          easing: 'easeOutExpo',
          rotate: true,
          scale: false,
          onAnimationComplete: null
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
      const data = [25, 25, 10, 10, 15, 5, 10]
      this.chartDataValues = data
    }
  }
}
</script>

<style scoped></style>
