<template>
  <v-hover>
    <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`">
      <v-img :aspect-ratio="16 / 9" :src="i.src">
        <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out black darken-2 v-card--reveal display-3 white--text"
            style="height: 100%;"
          >
            {{ i.version }}
          </div>
        </v-expand-transition>
      </v-img>

      <v-card-title>
        <div>
          <span class="headline">{{ i.name }}</span>
          <div class="d-flex">
            <v-rating
              :value="i.value"
              color="amber"
              dense
              half-increments
              readonly
              size="20"
            ></v-rating>
            <div class="ml-2 grey--text text--darken-2">
              <span>{{ i.value }}</span>
              <span>(year)</span>
            </div>
          </div>
        </div>
      </v-card-title>
      <v-card-text>
        <v-list two-line>
          <template v-for="(item, index) in i.subItems">
            <v-subheader v-if="item.header" :key="item.header">
              {{ item.header }}
            </v-subheader>

            <v-divider
              v-else-if="item.divider"
              :key="index"
              :inset="item.inset"
            ></v-divider>

            <v-list-tile v-else :key="item.title" avatar @click="click">
              <v-list-tile-avatar>
                <img :src="item.avatar" />
              </v-list-tile-avatar>

              <v-list-tile-content>
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
                <v-list-tile-sub-title
                  v-html="item.subtitle"
                ></v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </template>
        </v-list>
      </v-card-text>
    </v-card>
  </v-hover>
</template>

<script>
export default {
  props: {
    i: {
      type: Object,
      required: true
    }
  },
  methods: {
    click() {}
  }
}
</script>

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>
