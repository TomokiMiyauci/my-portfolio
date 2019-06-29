<template>
  <div>
    <v-container fluid grid-list-lg>
      <v-layout row wrap justify-space-around>
        <v-flex xs12 sm6 md4 xl4>
          <v-card color="grey">
            <v-card-title class="headline white--text">Acnorage</v-card-title>
            <v-card-text>
              <pie-chart :chart-data="chartData" :options="chartOptions" />
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs12 sm6 md4 xl4>
          <v-card color="grey">
            <v-card-title class="headline white--text">Acnorage</v-card-title>
            <v-card-text>
              <doughnut-chart :chart-data="chartData" :options="chartOptions" />
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>

      <div class="text-xs-center mt-2">
        <v-btn dark color="indigo" @click="randomizeData()"
          >Randomize data</v-btn
        >
      </div>
    </v-container>
    <v-container grid-list-xs>
      <v-career fluid>
        <v-career></v-career>
      </v-career>
    </v-container>
  </div>
</template>

<script>
import VCareer from '~/components/organisms/VCareer'
import colors from 'vuetify/es5/util/colors'

export default {
  components: {
    VCareer
  },
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
        elements: {
          center: {
            text: 'Desktop',
            color: '#36A2EB', // Default black
            fontStyle: 'Helvetica', // Default Arial
            sidePadding: 15 // Default 20 (as a percentage)
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
    this.randomizeData()
  },
  methods: {
    randomizeData: function() {
      const data = []
      for (let i = 0; i < this.chartLabels.length; i++) {
        data.push(Math.floor(Math.random() * 100))
      }
      this.chartDataValues = data
    }
  }
}
</script>
