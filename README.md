# Vuejs Image Gallery

#### Developed By Anamol Soman

[![Downloads](https://img.shields.io/npm/dm/vuejs-image-gallery.svg)](https://www.npmjs.com/package/vuejs-image-gallery) [![Version](https://img.shields.io/npm/v/vuejs-image-gallery.svg)](https://www.npmjs.com/package/vuejs-image-gallery)

![Capture4](https://user-images.githubusercontent.com/52847469/155925969-b6f69eb6-a9d9-4e8c-bf31-fd9034cef474.PNG)
![Capture](https://user-images.githubusercontent.com/52847469/155926118-1b27d2fb-74e4-4af3-8dd6-c6964a978a77.PNG)

|                                                      Tab View                                                      |                                                    Mobile View                                                     |
| :----------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------: |
| ![Capture3](https://user-images.githubusercontent.com/52847469/155926155-af36d4cf-8a24-4371-97e4-10cfba5cc455.PNG) | ![Capture2](https://user-images.githubusercontent.com/52847469/155926163-39cd82e7-33f2-4b1c-969e-276c6d59df0d.PNG) |

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
      :imageHeight="auto"
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

## License

MIT

**Free Software, Hell Yeah!**

[image-gallery]: https://github.com/anamolsoman/vuejs-image-gallery
