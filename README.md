# vuejs-image-gallery

![Screenshot from 2021-12-13 23-45-30](https://user-images.githubusercontent.com/52847469/145866506-c7b6c43d-8c06-4836-8a7a-82f6357e2d1a.png)

![Screenshot from 2021-12-13 23-45-42](https://user-images.githubusercontent.com/52847469/145866553-fec64c51-90a4-46f4-8533-72577001dad8.png)



In this project I created a npm package for dynamic and responsive image gallery
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
vue add vuetify
```

## Module

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

## Example

<a href="https://codesandbox.io/s/vuejs-image-gallery-1n6qb" target="">Check Demo</a>
