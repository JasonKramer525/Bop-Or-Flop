<template>
  <q-page>
    <div class="row justify-center full-height full-width text-center">
      <img
        class="q-mt-md"
        src="images/BopOrFlopInverse.png"
        style="max-width: 150px; height: auto;"
      />
    </div>
    <div class="row justify-center full-height full-width text-center">
      <p
        class="subtext text-h6"
        style="color:white"
      >Can you guess which song has more plays on Apple Music?</p>
    </div>

    <div class="row justify-center full-height full-width text-center q-mt-md">
      <q-btn
        class="q-px-xl q-py-xs subtext"
        color="green"
        size="30px"
        @click="$router.replace('/play')"
      >PLAY</q-btn>
    </div>

    <div class="flex bg-black justify-center">
      <img src="images/greenbars.gif" style="height: 300px;" />
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex"
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Rowdies:wght@700&display=swap");

.subtext {
  font-family: "Rowdies", cursive;
}
</style>
