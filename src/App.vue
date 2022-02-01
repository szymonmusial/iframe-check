<template>
  <div class="app">
    <show-iframe src="https://www.musialdev.pl/" />
  </div>
</template>

<script>
import ShowIframe from "./components/atoms/ShowIframe.vue";

export default {
  components: { ShowIframe },
  name: "App",
};
</script>

<style>
.app {
  width: 100%;
}

body {
  margin: 0px;
  padding: 0px;
  overflow: hidden;
}
</style>
