# Smoothslider

Welcome to Everybody!.
The best responsive slider. Period.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'smoothslider'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install smoothslider

## Usage
Import Bootstrap styles in app/assets/stylesheets/application.scss:
```scss
@import "smoothslider";
```

Require Bootstrap Javascripts in app/assets/javascripts/application.js:
```js
//= require smoothslider
```

How to use: 
1.Single page Smooth slider
```html
<a href="#menu1" class="scroll">Menu 1</a>
<a href="#menu2" class="scroll">Menu 2</a>
<a href="#menu3" class="scroll">Menu 3</a>

<div id="menu1"></div>
<div id="menu2"></div>
<div id="menu3"></div>
```
2.Basic Slider
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
  </ul>
</div>
```
```js
// Can also be used with $(document).ready()
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide"
  });
});
```
3.Basic Slider customDirectionNav
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
  </ul>
</div>
<div class="custom-navigation">
  <a href="#" class="flex-prev">Prev</a>
  <div class="custom-controls-container"></div>
  <a href="#" class="flex-next">Next</a>
</div>
```
```js
// Can also be used with $(document).ready()
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide",
    controlsContainer: $(".custom-controls-container"),
    customDirectionNav: $(".custom-navigation a")
  });
});
```
4.Basic Slider with Simple Caption
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
      <p class="flex-caption">Adventurer Cheesecake Brownie</p>
    </li>
    <li>
      <img src="slide2.jpg" />
      <p class="flex-caption">Adventurer Lemon</p>
    </li>
    <li>
      <img src="slide3.jpg" />
      <p class="flex-caption">Adventurer Donut</p>
    </li>
    <li>
      <img src="slide4.jpg" />
      <p class="flex-caption">Adventurer Caramel</p>
    </li>
  </ul>
</div>
```
```css
.flex-caption {
  width: 100%;
  padding: 2%;
  left: 0;
  bottom: 0;
  background: rgba(0,0,0,.5);
  color: #fff;
  text-shadow: 0 -1px 0 rgba(0,0,0,.3);
  font-size: 14px;
  line-height: 18px;
}
```
```js
// Can also be used with $(document).ready()
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide"
  });
});
```
5.Slider w/thumbnail controlNav pattern
```html
<div class="smoothslider">
  <ul class="slides">
    <li data-thumb="slide1-thumb.jpg">
      <img src="slide1.jpg" />
    </li>
    <li data-thumb="slide2-thumb.jpg">
      <img src="slide2.jpg" />
    </li>
    <li data-thumb="slide3-thumb.jpg">
      <img src="slide3.jpg" />
    </li>
    <li data-thumb="slide4-thumb.jpg">
      <img src="slide4.jpg" />
    </li>
  </ul>
</div>
```
```js
// Can also be used with $(document).ready()
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide",
    controlNav: "thumbnails"
  });
})
```
6.Slider w/thumbnail slider
```html
<div id="slider" class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
    <!-- items mirrored twice, total of 12 -->
  </ul>
</div>
<div id="carousel" class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
    <!-- items mirrored twice, total of 12 -->
  </ul>
</div>
```
```js
$(window).load(function() {
  // The slider being synced must be initialized first
  $('#carousel').smoothslider({
    animation: "slide",
    controlNav: false,
    animationLoop: false,
    slideshow: false,
    itemWidth: 210,
    itemMargin: 5,
    asNavFor: '#slider'
  });
 
  $('#slider').smoothslider({
    animation: "slide",
    controlNav: false,
    animationLoop: false,
    slideshow: false,
    sync: "#carousel"
  });
});

```
7.Basic Carousel
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
    <!-- items mirrored twice, total of 12 -->
  </ul>
</div>
```
```js
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide",
    animationLoop: false,
    itemWidth: 210,
    itemMargin: 5
  });
});
```
8.Carousel With Min & Max Ranges
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
    <!-- items mirrored twice, total of 12 -->
  </ul>
</div>
```
```js
$(window).load(function() {
  $('.smoothslider').smoothslider({
    animation: "slide",
    animationLoop: false,
    itemWidth: 210,
    itemMargin: 5,
    minItems: 2,
    maxItems: 4
  });
});
```
9.Carousel With Min & Max Ranges
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <img src="slide1.jpg" />
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
    <!-- items mirrored twice, total of 12 -->
  </ul>
</div>
```
```js
(function() {
 
  // store the slider in a local variable
  var $window = $(window),
      smoothslider = { vars:{} };
 
  // tiny helper function to add breakpoints
  function getGridSize() {
    return (window.innerWidth < 600) ? 2 :
           (window.innerWidth < 900) ? 3 : 4;
  }
 
  $(function() {
    SyntaxHighlighter.all();
  });
 
  $window.load(function() {
    $('.smoothslider').smoothslider({
      animation: "slide",
      animationLoop: false,
      itemWidth: 210,
      itemMargin: 5,
      minItems: getGridSize(), // use function to pull in initial value
      maxItems: getGridSize() // use function to pull in initial value
    });
  });
 
  // check grid size on resize event
  $window.resize(function() {
    var gridSize = getGridSize();
 
    smoothslider.vars.minItems = gridSize;
    smoothslider.vars.maxItems = gridSize;
  });
}());
```
10.Video & the api (vimeo)
```html
<div class="smoothslider">
  <ul class="slides">
    <li>
      <iframe id="player_1" src="https://player.vimeo.com/video/39683393?api=1&player_id=player_1" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
    </li>
    <li>
      <img src="slide2.jpg" />
    </li>
    <li>
      <img src="slide3.jpg" />
    </li>
    <li>
      <img src="slide4.jpg" />
    </li>
  </ul>
</div>
```
```js
// Can also be used with $(document).ready()
$(window).load(function() {
 
  // Vimeo API nonsense
  var player = document.getElementById('player_1');
  $f(player).addEvent('ready', ready);
 
  function addEvent(element, eventName, callback) {
    if (element.addEventListener) {
      element.addEventListener(eventName, callback, false)
    } else {
      element.attachEvent(eventName, callback, false);
    }
  }
 
  function ready(player_id) {
    var froogaloop = $f(player_id);
    froogaloop.addEvent('play', function(data) {
      $('.smoothslider').smoothslider("pause");
    });
    froogaloop.addEvent('pause', function(data) {
      $('.smoothslider').smoothslider("play");
    });
  }
 
 
  // Call fitVid before smoothslider initializes, so the proper initial height can be retrieved.
  $(".smoothslider")
    .fitVids()
    .smoothslider({
      animation: "slide",
      useCSS: false,
      animationLoop: false,
      smoothHeight: true,
      before: function(slider){
        $f(player).api('pause');
      }
  });
});
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/arjunghimire/smoothslider. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the smoothslider project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/arjunghimire/smoothslider/blob/master/CODE_OF_CONDUCT.md).
