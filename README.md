# Frontend Mentor - Pricing component with toggle solution

This is a solution to the [Pricing component with toggle challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/pricing-component-with-toggle-8vPwRMIC). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- Control the toggle with both their mouse/trackpad and their keyboard
- **Bonus**: Complete the challenge with just HTML and CSS

### Links

- Solution URL: [here](https://github.com/rafaeldevvv/pricing-component-wtth-toggle)
- Live Site URL: [here]([https://your-live-site-url.com](https://rafaeldevvv.github.io/pricing-component-wtth-toggle/))

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- SASS/SCSS
- JavaScript

### What I learned

I liked this way to make a toggle button.
```scss
#ckPricing {
   display: none;
}
.toggle-bar {
   display: flex;
   align-items: center;
   gap: 1.5em;
}
.toggle-button {
   display: block;
   width: 60px;
   height: 35px;
   position: relative;

   background: hsl(237, 63%, 64%);
   border-radius: 40px;

   cursor: pointer;
}
.toggle-button:hover {
   filter: brightness(1.3);
}
.toggle-button::before {
   content: '';
   position: absolute;
   height: 25px;
   aspect-ratio: 1;
   background: white;
   border-radius: 50%;

   left: 5px;
   top: 50%;
   transform: translateY(-50%);

   transition-property: transform, left;
   transition-duration: .2s;
}
#ckPricing:checked + .toggle-button::before {
   left: calc(100% - 5px);

   transform: translate(-100%, -50%);
}
```

This was my simple solution for the only-html-and-css version.
```scss
#prices:has(#ckPricing:checked) .annually {
   display:none;
}
```

I thought the boxes would shrink anyway with just flex-shrink of 1, but i also had to specify a min-width of 0.
```scss
.box {
  min-width: 0;
  flex: 1 1 auto;
}
```

### Continued development
I want to continue improving my skills of responsive web design and I want to use more utility classes.

### Useful resources

- [Stack Overflow](https://stackoverflow.com/questions/31292187/background-position-percentage-not-working#:~:text=The%20why,100%25%3B%20is%20bottom%20right.) - This helped me figure out how to position the background image.
- [Stack Overflow](https://stackoverflow.com/questions/38382734/flex-items-not-shrinking-when-window-gets-smaller) - This question helped me make the boxes shrink when I decreased the window size.

## Author

- Frontend Mentor - [@rafaeldevvv](https://www.frontendmentor.io/profile/rafaeldevvv)
- Instagram - [@rafaeldevvv](https://www.instagram.com/rafaeldevvv)
