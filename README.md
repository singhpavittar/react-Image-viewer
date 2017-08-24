# React Images Viewer

A simple react component for displaying an array of images.


### Quick start


```bash
npm install --save react-image-viewer
```

```jsx
import React from 'react';
import Blackbox from 'react-image-viewer';

export default class Example extends React.Component {
  ...
  render() {
    return (
      <Blackbox
        images={[{ src: 'http://example.com/img1.jpg' }, { src: 'http://example.com/img2.jpg' }]}
        isOpen={this.state.blackBoxIsOpen}
        onClickPrev={this.gotoPrevious}
        onClickNext={this.gotoNext}
        onClose={this.closeBlackbox}
      />
    );
  }
}
```

To build the examples locally, run:

```
npm install
npm start
```

Then open [`localhost:8000`](http://localhost:8000) in a browser.

Example using caption for the first image:

```jsx
<Blackbox
  images={Blackbox_IMAGE_SET}
  ...
/>

const BlackBox_IMAGE_SET = [
  {
    src: 'http://example.com/example/img1.jpg',
    caption: 'Sydney, Australia - Photo by Jill Smith',
  },
  {
    src: 'http://example.com/example/img2.jpg',
  }
];

```

## Options

Property	|	Type		|	Default		|	Description
:-----------------------|:--------------|:--------------|:--------------------------------
backdropClosesModal	|	bool	|	false	|	Allow users to exit the blackbox by clicking the backdrop
closeButtonTitle | string | ' Close (Esc) ' | Customize close esc title
enableKeyboardInput | bool  | true  | Supports keyboard input - <code>esc</code>, <code>arrow left</code>, and <code>arrow right</code>
currentImage  | number  | 0 | The index of the image to display initially
customControls | array | undefined | An array of elements to display as custom controls on the top of blackbox
images  | array | undefined | Required. An array of objects containing valid src and srcset values of img element
imageCountSeparator  | String  | ' of ' | Customize separator in the image count
isOpen  | bool  | false | Whether or not the blackbox is displayed
leftArrowTitle | string | ' Previous (Left arrow key) ' | Customize of left arrow title
onClickPrev | func | undefined | Fired on request of the previous image
onClickNext | func | undefined | Fired on request of the next image
onClose | func | undefined | Required. Handle closing of the blackbox
onClickImage | func | undefined | Handle click on image
onClickThumbnail | func | undefined | Handle click on thumbnail
preloadNextImage | bool | true | Based on the direction the user is navigating, preload the next available image
rightArrowTitle | string | ' Next (Right arrow key) ' | Customize right arrow title
showCloseButton | bool  | true | Optionally display a close "X" button in top right corner
showImageCount | bool  | true | Optionally display image index, e.g., "3 of 20"
width | number  | 1024 | Maximum width of the carousel; defaults to 1024px
hideArrow | bool | false | Show image arrow to change images
