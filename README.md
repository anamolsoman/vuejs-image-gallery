# vuejs-image-gallery

## Create Vue Project

```
vue create <Project-name>
```

## Project setup

```
npm install
```

## Install Vuetify

```
npm install
```

## Module

<<<<<<< HEAD

```
import Gallery from "vuejs-image-gallery";
```

```
export default {
name: "App",
data() {
return {
images: [
{ id: 1, imgSrc: require("@/assets/1.png") },
{ id: 2, imgSrc: require("@/assets/2.jpg") },
{ id: 3, imgSrc: require("@/assets/3.jpg") },
{ id: 4, imgSrc: require("@/assets/4.jpg") },
{ id: 5, imgSrc: require("@/assets/5.jpg") },
{ id: 5, imgSrc: require("@/assets/6.jpg") }
]
};
},
components: {
Gallery
}
};

```

## Usage

Once installed, it can be used in a template as simply as:

```

<Gallery v-bind:images="images" />
```

```
Example
```

![img](src/assets/Capture.png)

=======

### Git Repo

Link - https://github.com/anamolsoman/vuejs-image-gallery
