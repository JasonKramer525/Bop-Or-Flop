<template>
  <!---  <div class="overflow-hidden">
    <q-resize-observer @resize="onResize" :debounce="0" />

    <q-splitter
      class="fixed-center"
      id="photos"
      v-model="splitterModel"
      :limits="[0, 100]"
      :style="splitterStyle"
      before-class="overflow-hidden"
      after-class="overflow-hidden"
    >
      <template v-slot:before>
        <img
          transition-show="jump-down"
          transition-hide="jump-up"
          src="images/bruno.png"
          :width="width"
          class="absolute-top-left"
        />
      </template>

      <template v-slot:after>
        <img
          src="https://cdn.quasar.dev/img/parallax1-bw.jpg"
          :width="width"
          class="absolute-top-right"
        />
      </template>
    </q-splitter>
  </div> --->
  <div>
    <div class="row">
      <div class="col-lg-6 col-sm-12" style="color:white">
        <img src="images/cup.jpg" width="50%" class="absolute-top-right" />
      </div>

      <div class="col-lg-6 col-sm-12" style="color:white">
        <img
          transition-show="jump-down"
          transition-hide="jump-up"
          src="images/bruno.png"
          width="50%"
          class="absolute-top-left"
        />
      </div>
    </div>

    <q-avatar
      class="absolute-center subtext"
      size="100px"
      font-size="52px"
      color="green"
      text-color="white"
    >VS</q-avatar>

    <q-footer class="bg-green" elevated>
      <q-toolbar>
        <h4 class="subtext">Score:</h4>
        <q-space />
        <q-icon class="q-pa-sm" style="font-size: 5rem; color: red" name="fas fa-heart" />
        <q-icon class="q-pa-sm" style="font-size: 5rem; color: red" name="fas fa-heart" />
        <q-icon class="q-pa-sm" style="font-size: 5rem; color: red" name="fas fa-heart" />
      </q-toolbar>
    </q-footer>
  </div>
</template>

<script>
import { fasFont } from "@quasar/extras/fontawesome-v5";

export default {
  data() {
    return {
      width: 400,
      splitterModel: 50 // start at 50%
    };
  },

  methods: {
    // we are using QResizeObserver to keep
    // this example mobile-friendly
    onResize({ width }) {
      this.width = width;
    }
  },

  computed: {
    splitterStyle() {
      return {
        height: Math.min(1000, 0.66 * this.width) + "px",
        width: this.width + "px"
      };
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Rowdies:wght@700&display=swap");

.subtext {
  font-family: "Rowdies", cursive;
}
</style>
