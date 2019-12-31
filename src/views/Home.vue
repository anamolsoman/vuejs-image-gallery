<template>
  <div class="home">
    <Gallery v-bind:images="images" />
  </div>
</template>

<script>
// @ is an alias to /src
import Gallery from "@/components/Gallery.vue";

export default {
  data() {
    return {
      images: [
        { id: 1, imgSrc: require("../assets/1.png") },
        { id: 2, imgSrc: require("../assets/2.jpg") },
        { id: 3, imgSrc: require("../assets/3.jpg") },
        { id: 4, imgSrc: require("../assets/4.jpg") },
        { id: 5, imgSrc: require("../assets/5.jpg") },
        { id: 5, imgSrc: require("../assets/6.jpg") }
      ]
    };
  },
  components: {
    Gallery
  }
};
</script>
