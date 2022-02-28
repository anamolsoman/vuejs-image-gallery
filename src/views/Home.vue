<template>
  <div class="home">
    <Gallery
      :images="images"
      :imageWidth="imageWidth"
      :popUpMaxWidth="popUpMaxWidth"
      :mdCols="mdCols"
      :smCols="smCols"
      :xsCols="xsCols"
      :lgCols="lgCols"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import Gallery from "@/Gallery.vue";

export default {
  data() {
    return {
      imageWidth: 720,
      imageHeight: 450,
      popUpMaxWidth: 720,
      mdCols: 4,
      smCols: 4,
      xsCols: 6,
      lgCols: 2,

      images: [
        { id: 1, imgSrc: require("../assets/1.jpg") },
        { id: 2, imgSrc: require("../assets/2.jpg") },
        { id: 3, imgSrc: require("../assets/3.jpg") },
        { id: 4, imgSrc: require("../assets/4.jpg") },
        { id: 5, imgSrc: require("../assets/5.jpg") },
        { id: 6, imgSrc: require("../assets/6.jpg") },
        { id: 7, imgSrc: require("../assets/3.jpg") },
        { id: 8, imgSrc: require("../assets/5.jpg") }
      ]
    };
  },
  components: {
    Gallery
  }
};
</script>
