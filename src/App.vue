<template>
  <div id="app">
    <ImageZoom
      custom-class="my-custom-class"
      :scale="4"
      src="https://images.pexels.com/photos/4622893/pexels-photo-4622893.jpeg"
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
