<template>
  <div id="app">
    <ImageZoom
      custom-class="my-custom-class"
      :scale="4"
      src="https://tineye.com/images/widgets/mona.jpg"
    />
  </div>
</template>

<script>
import ImageZoom from "./components/ImageZoom.vue";

export default {
  name: "App",
  components: {
    ImageZoom,
  },
};
</script>
<style scoped>
.my-custom-class {
  border-radius: 100px;
}
</style>
