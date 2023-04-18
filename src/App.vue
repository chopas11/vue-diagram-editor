<template>
  <div class="App" @click="appEvents">
    <home-view />
  </div>
</template>

<script>
import HomeView from "@/pages/HomeView.vue";

export default {
  components: {
    HomeView,
  },
  methods: {
    appEvents(e) {
      let contextMenu = document.getElementsByClassName("contextMenu")[0];
      contextMenu.style.display = "none";
      console.log("appEvents!");
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
