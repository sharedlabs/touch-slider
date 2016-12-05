[![Build Status](https://img.shields.io/travis/sharedlabs/touch-slider.svg?style=flat-square)](https://travis-ci.org/sharedlabs/touch-slider)
[![License](https://img.shields.io/github/license/sharedlabs/touch-slider.svg?style=flat-square)](https://github.com/sharedlabs/touch-slider/blob/master/LICENSE.md)

_[Demo and API docs](https://sharedlabs.github.io/touch-slider/components/touch-slider/)_

# touch-slider

`touch-slider` is a super simple draggable slider for touch devices.

The drag doesn't work with mouse events. IMO for desktop it's better to have some arrow handles instead.

A slide is a container where you can attach content. There is always three slides attached at the same time, so animations can occur.

When a new slide is rendered the `new-slide` event is fired.  

Use the max attribute to set the max length of slides. 

```html
<touch-slider on-new-slide="_onNewSlide" max="[[images.length]]"></touch-slider>
...
_onNewSlide(event) {
  const slide = event.detail.slide;
  const slideIndex = event.detail.index;
  const img = document.createElement('img');

  img.setAttribute('src', this.images[slideIndex]);
  Polymer.dom(slide).appendChild(img);
}
```
