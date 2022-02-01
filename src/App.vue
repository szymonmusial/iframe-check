<template>
  <div class="app">
    <show-iframe src="http://localhost:8081/" />
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
