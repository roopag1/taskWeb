# Frontend Mentor - Coding bootcamp testimonials slider solution

This is a solution to the [Coding bootcamp testimonials slider challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/coding-bootcamp-testimonials-slider-4FNyLA8JL). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- Navigate the slider using either their mouse/trackpad or keyboard

### Screenshot

![](./images/Desktop-Testimonials.png)
![](./images/Mobile-Testimonials.png)

### Links

- Solution URL: [Frontend Mentor Live Solution](https://www.frontendmentor.io/solutions/testimonials-slider-solution-2mVX6EQ4VJ)
- Live Site URL: [Testimonial Slider Site](https://michaelr47.github.io/Testimonials-Slider/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox

### What I learned

Used these two functions to slide to next/prev slide.

```js
function changeToPrevImage() {
  slidingIdx--;

  elements.map(el => {
    el.style.animation = 'rightToLeft 1.5s';
  })

  if (slidingIdx < 0) {
    slidingIdx = testimonies.length - 1;
  }

  quote.innerText      = testimonies[slidingIdx].quote;
  personName.innerText = testimonies[slidingIdx].id;
  occupation.innerText = testimonies[slidingIdx].occupation;
  img.src              = testimonies[slidingIdx].imageURL;

}
// changes to next testimony
function changeToNextImage() {
  slidingIdx++;
  elements.map(el => {
    el.style.animation = 'leftToRight 1.5s';
  })
  
  if (slidingIdx === testimonies.length) {
    slidingIdx = 0;
  }

  quote.innerText      = testimonies[slidingIdx].quote;
  personName.innerText = testimonies[slidingIdx].id;
  occupation.innerText = testimonies[slidingIdx].occupation;
  img.src              = testimonies[slidingIdx].imageURL;
}
```

## Author
- Frontend Mentor - [michaelr47](https://www.frontendmentor.io/profile/michaelr47)
