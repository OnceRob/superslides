# Superslides 0.4.3 - [changelog](https://github.com/nicinabox/superslides/blob/master/changelog.md)

Superslides is a full screen slider for jQuery heavily influenced by Nathan Searles' [SlidesJS](https://github.com/nathansearles/slides/). It's designed to be as flexible as possible, while maintaining a reasonable code base and good browser compatibility.

It's 4.3kb minified (9.4kb uncompressed).

## Usage
[Check out the demo](http://nicinabox.github.com/superslides/) for a complete example. Basic usage is as follows. See options below for things you can change.

    $('#slides').superslides(options_hash)

## Options

There are a few configurable options (these are the defaults):

    play: false
    slide_speed: 'normal'
    slide_easing: 'linear'
    pagination: true
    hashchange: false
    scrollable: true
    classes:
      nav: 'slides-navigation'
      container: 'slides-container'
      pagination: 'slides-pagination'

## Events

Superslides triggers a few events that you can bind to.

    init.slides
    started.slides
    animated.slides
    updated.slides

## API

    $('#slides').superslides('start')
    $('#slides').superslides('stop')
    $('#slides').superslides('animate' [, index|'next'|'prev'])
    $('#slides').superslides('size')
    $('#slides').superslides('destroy')
    $('#slides').superslides('update')

If add slides after it's initialized (a la ajax), be sure to call `update`.

## Markup

Markup is pretty straightforward. At minimum it looks like this:

    <div id="slides">
      <div class="slides-container">
        <img src="http://flickholdr.com/1000/800" alt="">
        <img src="http://flickholdr.com/1000/800" alt="">
      </div>
    </div>

You could even use a UL as the `slides-container`

    <div id="slides">
      <ul class="slides-container">
        <li>
          <img src="http://flickholdr.com/1000/800" alt="">
          <div class="container">
            Slide one
          </div>
        </li>
        <li>
          <img src="http://flickholdr.com/1000/800/space" alt="">
          <div class="container">
            Slide two
          </div>
        </li>
        <li>
          <img src="http://flickholdr.com/1000/800/tech" alt="">
          <div class="container">
            Slide three
          </div>
        </li>
      </ul>
      <nav class="slides-navigation">
        <a href="#" class="next">Next</a>
        <a href="#" class="prev">Previous</a>
      </nav>
    </div>

## Hardware Acceleration

Superslides is compatible with the [jQuery Animate Enhanced](http://playground.benbarnett.net/jquery-animate-enhanced/) plugin. Simply include it before this plugin and it will automatically smooth out transitions using CSS instead of JavaScript.

## Contributing

Check contributing.md.