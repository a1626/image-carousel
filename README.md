
[![License](http://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/a1626/image-carousel/blob/master/LICENSE)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/a1626/image-carousel)
[![Travis](https://img.shields.io/travis/rust-lang/rust.svg)](https://travis-ci.org/a1626/image-carousel)



# \<image-carousel\>

It's a carousel element for Polymer 2.0.

## Installation

```
  bower i --save image-carousel
```

## Example


```html
<image-carousel aria-label="example carousel">
  <template is="dom-repeat" items='["https://c2.staticflickr.com/2/1217/4607963354_e1a8fea210_z.jpg", "http://www.hdwallpapery.com/static/images/1391099215267_hero2_niQ3B7S.jpg", "https://tse4.mm.bing.net/th?id=ORT.TH_470633631&pid=1.12&eid=G.470633631"]' slot="images">
    <img src="[[item]]" class="scrolling-images" alt$="demo image alt [[index]]" width="100%" height="374px">
  </template>
</image-carousel>
```

## Usage

Please keep following points in mind while using the element

- As images will be part of `light-dom` please add property/attribute `slot="image"` to the container of the images (template in above example).
- Images should have class named `scrolling-images` (Defining the class in not necessary, just add the attribute to image element).
- In case, you want to change images dynamically do call `computeNumberOfImages` function afterwards.  Carousel will fire `image-carousel-changed` event once all the changes are done. You can listen for it to do/read any further changes.


```javascript
// assuming id of image-carousel element on which change needs to be done is image-carousel
this.$['image-carousel'].addEventListener('image-carousel-changed', () => {
  //further action goes here
});
```

- As efforts have been made to keep this element accessible please add `alt` attribute to image tag and [aria-label](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute) or [aria-labelledby](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-labelledby_attribute) to image-carousel.

## Web Accessibility

Web accessibility refers to practice of making web easily usable/accessible for people with disabilities. [Here](https://twitter.com/captainsafia/status/871056480799162368?ref_src=twsrc%5Etfw&ref_url=https%3A%2F%2Faxesslab.com%2Faccessibility-according-to-pwd%2F) is a recent twitter post where people with disability tweeted `what's the hardest thing about browsing the web`, or if you like to read accumulated version please refer to [this](https://axesslab.com/accessibility-according-to-pwd?utm_source=ponyfoo+weekly&utm_medium=email&utm_campaign=issue-71) article.

Implementing accessibility (also known as WAI-ARIA, ARIA, a11y) in your project isn't as tough as it may look, it has been well documented by w3c and you read the documentation [here](https://www.w3.org/TR/wai-aria-1.1/#usage). You can also look at some of there [examples](https://www.w3.org/WAI/tutorials/). If you like you can also follow [these](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) video tutorials posted on youtube by @robdodson.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## License

MIT License
