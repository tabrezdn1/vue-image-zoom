# vue-image-zoom

## Purpose
This is a vue component that zooms in on an image when hovered, can be used in portfolios, gallery, and e-commerce application.


### Example
#### Minimalistic example
```
<ImageZoom src="https://images.pexels.com/photos/4622893/pexels-photo-4622893.jpeg" />
```
#### Full fledged example
```
<template>
  <div id="app">
    <ImageZoom
      custom-class="my-custom-class"
      :scale="4"
      height="800px"
      width="800px"
      src="https://images.pexels.com/photos/4622893/pexels-photo-4622893.jpeg"
    />
  </div>
</template>

<script>
import ImageZoom from "@tabrezdn1/vue-image-zoom";

export default {
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
```


### Props
There are currently the following props:

| Prop | type | Description | Required | Default |
| ------ | ------ | ------ | ------ | ------ |
| src | String | This is the source url for the image | `true` | As it is required prop so - `null` |
| height | String | This prop is used to specify the height of the div where image will render. You can use it to specify custom height for the frame | `false` | `500px` |
| width | String | This prop is used to specify the width of the div where image will render. You can use it to specify custom width for the frame | `false` |`500px` |
| customClass | String | This is name of the class that you want to apply on the parent element of the component, for example a custom-class | `false` | `''` |
| scale | Number | This prop specifies the amount of zoom to be done. Consider it like zoom `x`. For Example if you pass 2, it will zoom 2x times that is twice. | `false` | `2` |

## Documentation
Coming soon...
