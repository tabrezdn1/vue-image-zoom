<template>
  <div id="app">
    <ImageZoom
      custom-class="my-custom"
      :scale="4"
      src="https://images.unsplash.com/photo-1582769923195-c6e60dc1d8dc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80"
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
