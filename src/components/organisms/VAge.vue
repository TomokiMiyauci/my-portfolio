<template>
  <v-card color="grey">
    <v-card-title class="headline white--text">Age</v-card-title>
    <v-card-text>
      <span class="number white--text">
        25
        <sup>y.o.</sup>
      </span>

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
      chartColors: [colors.red.lighten1, colors.transparent],
      chartOptions: {
        cutoutPercentage: 90,
        tooltips: {
          enabled: false
        },
        maintainAspectRatio: false,
        animation: {
          duration: 1500,
          steps: 100,
          easing: 'easeOutBounce',
          rotate: true,
          scale: false,
          onAnimationComplete: null
        },

        legend: {
          display: false
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
            backgroundColor: this.chartColors,
            borderWidth: 0,
            hoverBackgroundColor: [colors.red.darken1, colors.transparent]
          }
        ]
      }
    }
  },
  mounted: function() {
    this.initalize()
  },
  methods: {
    initalize() {
      const data = [25, 35]
      this.chartDataValues = data
    }
  }
}
</script>

<style scoped>
span {
  font-size: 70px;
  position: absolute;
  top: 0;
  left: 0;
  margin: auto;
  right: 0;
  margin: auto;
  text-align: center;
  top: 58%;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
}
</style>
