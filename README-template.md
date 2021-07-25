# Frontend Mentor - Ping coming soon page solution

This is a solution to the [Ping coming soon page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/ping-single-column-coming-soon-page-5cadd051fec04111f7b848da). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Ping coming soon page solution](#frontend-mentor---ping-coming-soon-page-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Submit their email address using an `input` field
- Receive an error message when the `form` is submitted if:
	- The `input` field is empty. The message for this error should say *"Whoops! It looks like you forgot to add your email"*
	- The email address is not formatted correctly (i.e. a correct email address should have this structure: `name@host.tld`). The message for this error should say *"Please provide a valid email address"*

### Screenshot

**Mobile**

<img src="images/../screenshots/mobile.png" height=500 style="padding-right: 20px" alt="mobile-view">
<img src="images/../screenshots/mobile-error.png" height=500 alt="mobile-view with error">

**Desktop**

<img src="images/../screenshots/desktop.png" height=500 alt="Desktop view">

### Links

- Solution URL: [Github](https://github.com/gylim0604/FrontEnd-Mentor-Ping-coming-soon)
- Live Site URL: [Vercel](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow
- SCSS
- Javascript

### What I learned

Mostly a fast project, so I used this chance to properly learn how to manipulate svgs. 
So here are some findings: 
- 1 SVGs can be used in multiple ways, the way I prefer is by importing them through xlink, with the SVG def stored in an external file. Here is an example:
  ```
  <svg class="icon">
      <use
          xlink:href="images/twitter.svg#icon-twitter"
      ></use>
  </svg>
  ```
  For the SVG to work this way, it has to be saved with the def tags.
  ```html
  <svg>
    <defs>
      <symbol id="icon-facebook" viewBox="0 0 32 32">
        <path d="M19 6h5v-6h-5c-3.86 0-7 3.14-7 7v3h-4v6h4v16h6v-16h5l1-6h-6v-3c0-0.542 0.458-1 1-1z"></path>
      </symbol>
    </defs>
  </svg>
  ```
  I think majority of SVGs do not include this when you download them, so it would be good to take note.

- 2 Importing SVGs through xlink allows very easy manipulation with the CSS. 
  For example, to change the color of the SVG, all we need is just this line of code.
  ```css
  .icon {
        
        fill: $blue;
    }
  ```
Another thing I learned was that the pseudo-elements ::after and ::before does not work with the \<input> tag. This is because the pseudo-elements only work on **container** elements i.e. 
\<div>, \<label> etc. The \<input> element is unfortunately not considered a "container" element. 



### Useful resources

- [Vecta.io](https://vecta.io/blog/best-way-to-embed-svg),[svgontheweb.com](https://svgontheweb.com/) - These two articles helped me understand SVGs more in depth
- [scottohara.me](https://www.scottohara.me/blog/2014/06/24/pseudo-element-input.html) - This post on the blog helped me understand why the ::after element wasn't working with my \<input>

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author
- Frontend Mentor - [@gylim0604](https://www.frontendmentor.io/profile/gylim0604)

