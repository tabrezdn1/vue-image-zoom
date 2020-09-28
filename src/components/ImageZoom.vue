<template>
  <div
    :class="containerClass"
    :style="containerStyle"
    @mousemove="mouseMove($event)"
    @mouseleave="mouseLeave($event)"
  >
    <img
      :src="imageSource"
      :style="zoomStyle"
      alt="vue-image-zoom cannot find image"
    />
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
    height: {
      type: String,
      default: "500px",
    },
    width: {
      type: String,
      default: "500px",
    },
    customClass: {
      type: String,
      default: "",
    },
    scale: {
      type: Number,
      default: 2,
    },
  },
  data() {
    return {
      imageSource: null,
      zoomStyle: {
        transformOrigin: "center center",
        transform: "scale(1)",
        objectFit: "cover",
        height: "100%",
        width: "100%",
      },
      containerStyle: {
        overflow: "hidden",
      },
      zoomScale: null,
      containerClass: "",
    };
  },
  mounted() {
    this.initData();
  },
  methods: {
    initData() {
      this.imageSource = this.src;
      this.containerStyle.height = this.height;
      this.containerStyle.width = this.width;
      this.zoomScale = this.scale;
      this.containerClass = this.customClass;
    },
    mouseMove(e) {
      const x = e.clientX - e.target.offsetLeft;
      const y = e.clientY - e.target.offsetTop;

      this.zoomStyle.transformOrigin = `${x}px ${y}px`;
      this.zoomStyle.transform = `scale(${this.zoomScale})`;
    },
    mouseLeave() {
      this.zoomStyle.transformOrigin = "center center";
      this.zoomStyle.transform = "scale(1)";
    },
  },
};
</script>