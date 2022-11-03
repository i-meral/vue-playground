<template>
  <v-card>
    <v-tabs
      v-model="tab"
      bg-color="primary"
    >
      <v-tab value="one">Item One</v-tab>
      <v-tab value="two">Item Two</v-tab>
      <v-tab value="three">Item Three</v-tab>
    </v-tabs>

    <v-card-text>
      <v-window v-model="tab">
        <v-window-item value="one">
          <OneWorld/>
        </v-window-item>

        <v-window-item value="two">
          <TwoWorld/>
        </v-window-item>

        <v-window-item value="three">
          <ThreeWorld/>
        </v-window-item>
      </v-window>
    </v-card-text>
  </v-card>
</template>
<script>
import OneWorld from './OneWorld.vue';
import ThreeWorld from './ThreeWorld.vue';
import TwoWorld from './TwoWorld.vue';

  export default {
    data: () => ({
        tab: null,
    }),
    components: { OneWorld, TwoWorld, ThreeWorld }
}
</script>