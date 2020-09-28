<template>
  <div @mousemove="mouseMove()" @mouseleave="mouseLeave()">
    <img :src="imageSource" alt="vue-image-zoom cannot find image">
  </div>
</template>

<script>
export default {
  name: "ImageZoom",
  props: {
    src: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      imageSource: null,
    };
  },
  mounted() {
    this.initData();
  },
  methods: {
    initData() {
      this.imageSource = this.src;
    },
    mouseMove(){

    },
    mouseLeave(){
      
    }
  },
};
</script>

<style>
</style>