# Vuejs Image Gallery

#### Developed By Anamol Soman

[![Downloads](https://img.shields.io/npm/dm/vuejs-image-gallery.svg)](https://www.npmjs.com/package/vuejs-image-gallery) [![Version](https://img.shields.io/npm/v/vuejs-image-gallery.svg)](https://www.npmjs.com/package/vuejs-image-gallery)

|                                                                 Image Listing                                                                 |                                                                  Image View                                                                   |
| :-------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: |
| ![Screenshot from 2021-12-13 23-45-30](https://user-images.githubusercontent.com/52847469/145866506-c7b6c43d-8c06-4836-8a7a-82f6357e2d1a.png) | ![Screenshot from 2021-12-13 23-45-42](https://user-images.githubusercontent.com/52847469/145866553-fec64c51-90a4-46f4-8533-72577001dad8.png) |

Vuejs image gallery is a responsive and customizable image gallery.

## Features

- Simple and attractive
- Customizable
- Fully Responsive

## Tech

Image gallery uses a number of open source projects to work properly:

- [Vuejs] - JavaScript framework
- [Vuetify] - UI library

And of course Dillinger itself is open source with a [public repository][image-gallery]
on GitHub.

## Installation

Install the dependencies and devDependencies and start the server.

```sh
npm install vuejs-image-gallery
```

## Customization

Vuejs image gallery is having some customizable options so you can make changes as per your requirements.

| Props         | Values                                               |
| ------------- | ---------------------------------------------------- |
| images        | Array of object which contain id and url of image    |
| imageWidth    | Width of popup image                                 |
| imageHeight   | Height of popup image                                |
| popUpMaxWidth | Maximum width of the popup                           |
| mdCols        | Number of images you want in medium screen size      |
| smCols        | Number of images you want in small screen size       |
| xsCols        | Number of images you want in extra small screen size |
| lgCols        | Number of images you want in large screen size       |

## Usage

Import the component like this

```sh
import Gallery from "vuejs-image-gallery";
```

Add the component in your template

```sh
 <Gallery
      :images="images"
      :imageWidth="720"
      :imageHeight="450"
      :popUpMaxWidth="720"
      :mdCols="4"
      :smCols="4"
      :xsCols="6"
      :lgCols="2"
    />
```

Pass the required data in script

```sh
export default {
    name: "App",
    data() {
        return {
            images: [{
                    id: 1,
                    imgSrc: require("@/assets/1.png")
                },
                {
                    id: 2,
                    imgSrc: require("@/assets/2.jpg")
                },
                {
                    id: 3,
                    imgSrc: require("@/assets/3.jpg")
                },
                {
                    id: 4,
                    imgSrc: require("@/assets/4.jpg")
                },
                {
                    id: 5,
                    imgSrc: require("@/assets/5.jpg")
                },
                {
                    id: 6,
                    imgSrc: require("@/assets/6.jpg")
                }
            ]
        };
    },
    components: {
        Gallery
    }
};
```

In image src you can pass location of your source

> Note: `Id should be in proper numbers

## License

MIT

**Free Software, Hell Yeah!**

[image-gallery]: https://github.com/anamolsoman/vuejs-image-gallery
