<template>
  <div class="iframe">
    <iframe :src="src" class="intranet" frameborder="0" id="test"></iframe>
  </div>
  <button @click="getIframeContent('test')" class="button">ZAŁADUJ TREŚĆ Z I FRAME</button>
</template>

<script>
export default {
  props: {
    src: String,
  },
  setup() {
    const getIframeContent = (frameId) => {
      const iframe = document.querySelector("#" + frameId);
      const frameContent = iframe.contentWindow.document.body.innerHTML;

      console.log(frameContent);
    };

    return { getIframeContent };
  },
};
</script>

<style scoped>
iframe {
  width: 80%;
  height: 90vh;
}
</style>
