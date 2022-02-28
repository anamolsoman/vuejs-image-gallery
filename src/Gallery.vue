<template>
  <v-container data-app="true">
    <v-row>
      <v-col
        v-for="(image, index) in images"
        :key="index"
        :md="mdCols"
        :sm="smCols"
        :cols="xsCols"
        :lg="lgCols"
      >
        <v-card>
          <v-img
            :src="image.imgSrc"
            @click.stop="dialogBox(image)"
            aspect-ratio="1"
            class="grey lighten-2"
          >
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular
                  indeterminate
                  color="grey lighten-5"
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-card>
      </v-col>
      <v-dialog v-model="dialog" :width="popUpMaxWidth">
        <v-btn @click="dialog = false" width="20px" class="close-button" text>
          <v-icon class="red--text">mdi-close</v-icon>
        </v-btn>
        <v-card flat class="image-card">
          <v-img
            :src="imgSrc"
            :width="imageWidth"
            :height="imageHeight"
          ></v-img>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              class="left-button"
              fab
              small
              outlined
              text
              @click="moveToLeft()"
              ><v-icon>mdi-arrow-left</v-icon></v-btn
            >
            <v-btn
              class="right-button"
              fab
              small
              outlined
              text
              @click="moveToRight()"
              ><v-icon>mdi-arrow-right</v-icon></v-btn
            >
            <v-spacer></v-spacer>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    images: {
      type: Array
    },
    imageWidth: {
      type: Number,
      default: 720
    },
    imageHeight: {
      type: Number || String,
      default: "auto"
    },
    popUpMaxWidth: {
      type: Number,
      default: 720
    },
    lgCols: {
      type: Number,
      default: 2
    },
    mdCols: {
      type: Number,
      default: 4
    },
    smCols: {
      type: Number,
      default: 4
    },
    xsCols: {
      type: Number,
      default: 6
    }
  },
  data() {
    return {
      dialog: false,
      imgSrc: "",
      image_id: "",
      show: true
    };
  },
  methods: {
    dialogBox(image) {
      this.dialog = true;
      this.image_id = image.id;
      this.imgSrc = image.imgSrc;
    },
    moveToRight() {
      var lastElement = this.images[this.images.length - 1];
      if (lastElement.id >= this.image_id + 1) {
        this.image_id = this.image_id + 1;
        var newitem = this.images.find(item => item.id === this.image_id);
        this.imgSrc = newitem.imgSrc;
      }
    },
    moveToLeft() {
      if (this.images[0].id <= this.image_id - 1) {
        this.image_id = this.image_id - 1;
        var newitem = this.images.find(item => item.id === this.image_id);
        this.imgSrc = newitem.imgSrc;
      }
    }
  }
};
</script>
<style scoped>
.close-button {
  position: absolute;
  z-index: 1;
  margin: auto;
}
.action {
  display: block;
}
</style>
