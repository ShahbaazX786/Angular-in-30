## Swiper Js is a feature rich carousel library.

##### steps to install:
1. Goto this [link](https://swiperjs.com/) > getting started.
2. We can install and use via npm but it requires a lot of configuring.
3. So we can just use CDN links of swiper css and JS and we are good to go.
- Note: It supports react,angular,vue,element(angular replacement in v9).
- From v9 of swiperjs angular support is removed but we can just use lower version or just use CDN and apply core api logic of swiper to use all features of it.

##### Using swiper:
1. We need to follow certain syntax to use swiper features.

```HTML
<!-- Slider main container -->
<div class="swiper mySwiper">
  <!-- Additional required wrapper -->
  <div class="swiper-wrapper">
    <!-- Slides -->
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
    ...
  </div>
  <!-- If we need pagination -->
  <div class="swiper-pagination"></div>

  <!-- If we need navigation buttons -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>

  <!-- If we need scrollbar -->
  <div class="swiper-scrollbar"></div>
</div>

```

2. We need to initialize swiper before we can use its functionality in various ways:
- Internal script link (at bottom of the body tag)[Doesn't work in angular components]
- External script link (at bottom of the body).
> Note: To Use the swiper external js file in angular component at runtime(dynamically) then we gotta follow a certain approach explained in detail [here](../Libraries/Using-External-JS-in-Angular-Components.md)

##### Initializing Swiper.js file.
- We need to create a swiper.js file in assets folder and load , use it runtime using method#4 in this [article](../Libraries/Using-External-JS-in-Angular-Components.md)
###### Swiper.js code :
```javascript
 
var swiper = new Swiper(".mySwiper", {
    slidesPerView: 3, // these are called as parameters
    spaceBetween: 25, 
    centerSlide: 'true',
    fade: 'true',
    grabCursor: 'true',
    pagination: {
      el: ".swiper-pagination",
      clickable: true,
      dynamicBullets: true,
    },
    navigation: {
      nextEl: ".swiper-button-next",
      prevEl: ".swiper-button-prev",
    },

    breakpoints:{
        0: {
            slidesPerView: 1,
        },
        520: {
            slidesPerView: 2,
        },
        950: {
            slidesPerView: 3,
        },
    },
  });

```

##### Parameters of Swiperjs:
- slidesPerView: 1, --> This indicates slides visible in the page.
- spaceBetween: 30, --> This is the distance bw two slides.
- loop: true, --> This makes the slides scroll infinitely(repeats list from left to right and vice-versa).
- centerSlide: 'true', --> Makes a slide to be in the center.
- fade: 'true', --> Adds a fade transition effect
- grabCursor: 'true', --> Makes **cursor:grab** if we hover on slides.
- There are other modules too which you can customize (ex:pagination, navigation, scrollbar)
Follow [This link](https://swiperjs.com/swiper-api) for Swiper API and detailed up to date tutorial.