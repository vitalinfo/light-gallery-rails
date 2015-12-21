# jQuery lightGallery Rails
Ruby on Rails wrapper for [jQuery lightGallery](https://github.com/sachinchoolur/lightGallery) 

Description
----------------
JQuery lightGallery is a lightweight jQuery lightbox gallery for displaying image and video galleries

How to use lightGallery?
--------------------

## Installation

Add the following code to your Gemfile:

```ruby
gem 'light_gallery_rails', git: 'https://github.com/JoJoS003/light-gallery-rails.git'   
```

Include the following code into your `application.js`

```javascript
//= require light-gallery
```

Include the following code into your `application.css`

```css
*= require light-gallery
```

### HTML Structure ###
lightgallery does not force you to use any kind of markup. you can use whatever markup you want. But i suggest you to use the following markup. Here you can find the detailed examples of deferent kind of markups.
```html
<div id="lightgallery">
  <a href="img/img1.jpg">
      <img src="img/thumb1.jpg" />
  </a>
  <a href="img/img2.jpg">
      <img src="img/thumb2.jpg" />
  </a>
  ...
</div>
```
### Call lightGallery! ###
```html
<script type="text/javascript">
  $(document).ready(function() {
    $("#lightGallery").lightGallery(); 
  });
</script>
```
### Play with settings ###
```html
    <script type="text/javascript">
      $(document).ready(function() {
        $("#lightGallery").lightGallery({

          mode: 'slide',
          useCSS: true,
          cssEasing: 'ease', //'cubic-bezier(0.25, 0, 0.25, 1)',//
          easing: 'linear', //'for jquery animation',//
          speed: 600,
          addClass: '',

          closable: true,
          loop: false,
          auto: false,
          pause: 4000,
          escKey: true,
          controls: true,
          hideControlOnEnd: false,

          preload: 1, //number of preload slides. will exicute only after the current slide is fully loaded. ex:// you clicked on 4th image and if preload = 1 then 3rd slide and 5th slide will be loaded in the background after the 4th slide is fully loaded.. if preload is 2 then 2nd 3rd 5th 6th slides will be preloaded.. ... ...
          showAfterLoad: true,
          selector: null,
          index: false,

          lang: {
              allPhotos: 'All photos'
          },
          counter: false,

          exThumbImage: false,
          thumbnail: true,
          showThumbByDefault:false,
          animateThumb: true,
          currentPagerPosition: 'middle',
          thumbWidth: 100,
          thumbMargin: 5,


          mobileSrc: false,
          mobileSrcMaxWidth: 640,
          swipeThreshold: 50,
          enableTouch: true,
          enableDrag: true,

          vimeoColor: 'CCCCCC',
          videoAutoplay: true,
          videoMaxWidth: '855px',

          dynamic: false,
          dynamicEl: [],

          // Callbacks el = current plugin
          onOpen        : function(el) {}, // Executes immediately after the gallery is loaded.
          onSlideBefore : function(el) {}, // Executes immediately before each transition.
          onSlideAfter  : function(el) {}, // Executes immediately after each transition.
          onSlideNext   : function(el) {}, // Executes immediately before each "Next" transition.
          onSlidePrev   : function(el) {}, // Executes immediately before each "Prev" transition.
          onBeforeClose : function(el) {}, // Executes immediately before the start of the close process.
          onCloseAfter  : function(el) {}, // Executes immediately once lightGallery is closed.
                
        });
    });
    </script>
```

In-depth explanation of settings can be found on a [separate page](http://sachinchoolur.github.io/lightGallery/settings.html).

### Public methods ###
```html
    <script type="text/javascript">
    $(document).ready(function() {
        var gallery = $("#lightGallery").lightGallery();
        gallery.isActive(); //check active state of lightGallery;
        gallery.destroy(); //to destroy the plugin on the given element.
    });
    </script>
```

Versioning
--------------------
Version numbers will mirror the corresonding version of the [jQuery lightGallery](https://github.com/sachinchoolur/lightGallery) release used within this wrapper. 

.
