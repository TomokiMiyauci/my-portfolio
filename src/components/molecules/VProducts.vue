<template>
  <v-container grid-list-xs pa-5>
    <p class="text-xs-center headline">- Products -</p>
    <v-layout row wrap justify-space-around pa-5>
      <v-flex v-for="i in 2" :key="i" xs4>
        <v-card>
          <v-img
            :src="require('~/assets/logo/awesome-investor.jpg')"
            :aspect-ratio="16 / 9"
          ></v-img>
          <v-card-title>
            <span class="headline">Awesome Investor</span>
          </v-card-title>
          <v-card-text>
            <span
              >Internal management system of investment management company</span
            >

            <v-expansion-panel popout>
              <v-expansion-panel-content v-for="(item, i) in 2" :key="i">
                <template v-slot:header>
                  <v-subheader>Feature</v-subheader>
                </template>
                <v-card>
                  <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
                    do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </v-card-text>
                </v-card>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {}
</script>

<style></style>
