<template>
  <v-container>
    <v-layout>
      <v-flex>
        <v-card class="elevation-0 transparent">
          <v-card-title>
            <div class="headline">Contact Me</div>
          </v-card-title>
          <v-card-text
            >If you are interested in me, please contact me.</v-card-text
          >
          <v-list class="transparent">
            <v-list-tile v-for="item in items" :key="item.icon">
              <v-list-tile-action>
                <v-icon class="red--text">{{ item.icon }}</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>{{ item.text }}</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      { icon: 'person', text: 'Tomoki Miyauchi' },
      { icon: 'place', text: 'Tokyo, JA' },
      { icon: 'email', text: 'development.operation.6.6.6@gmail.com' }
    ]
  })
}
</script>

<style></style>
