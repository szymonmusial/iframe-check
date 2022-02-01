<template>
  <div class="iframe">
    <iframe :src="src" class="intranet" frameborder="0" id="test"></iframe>
  </div>
  <button @click="delBlank" class="button">ZAŁADUJ TREŚĆ Z I FRAME</button>
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
  width: calc(100% - 64px);
  height: calc(100vh - 64px);
  margin: 32px;
  border: 1px solid black;
}

.button {
  position: absolute;
  padding: 16px 64px;
  left: 50%;
  bottom: 4px;
  background-color: rgb(17, 17, 114);
  color: #fff;
  transform: translate(-50%, 0);
  border: 0px;
}
</style>
