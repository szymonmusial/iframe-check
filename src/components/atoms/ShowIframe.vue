<template>
  <div class="iframe">
    <iframe :src="src" class="intranet" frameborder="0" width="100%"></iframe>
  </div>
</template>

<script>
export default {
  props: {
    src: String,
  },
};
</script>

<style scoped>
iframe {
  width: 100%;
  height: 100vh;
}
</style>
