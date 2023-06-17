# Frontend Mentor - Art gallery website solution

This is a solution to the [Art gallery website challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/art-gallery-website-yVdrZlxyA). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for each page depending on their device's screen size
- See hover states for all interactive elements throughout the site
- **Bonus**: Use Leaflet JS to create an interactive location map with custom location pin

### Screenshot

Coming soon...

<!-- ![Desktop Preview](/public/screenshots/dekstop-preview.png)

![Desktop Preview in 3D](/public/screenshots/desktop-preview-3d.png)

![Mobile Preview in 3D](/public/screenshots/mobile-preview-3d.png) -->

### Links

- Solution URL: [GitHub Code](https://github.com/dostonnabotov/fem_art-gallery-website/)
- Live Site URL: [Live Preview](https://technophile-art-gallery-website.netlify.app/)

## My process

### Built with

- HTML
- CSS
- [Vite](https://vitejs.dev/)
- [Prettier](https://prettier.io/)
- [Fluid typography - Utopia](https://utopia.fyi/type/calculator/)
- [Leaflet JS](https://leafletjs.com/) - *Coming soon...*

### What I learned

- Using [CSS `text-wrap: balance`](https://caniuse.com/css-text-wrap-balance) to balance the headings:

```css
h1,
h2,
h3 {
  text-wrap: balance;
}
```

- Optimizing images by converting them to webp format:

```html
<picture>
  <source
    media="(min-width: 640px)"
    srcset="/images/old-woman-gallery-desktop.webp"
    type="image/webp"
  />
  <source
    media="(min-width: 640px)"
    srcset="/images/old-woman-gallery-desktop.jpg"
    type="image/jpeg"
  />
  <img
    src="/images/old-woman-gallery-mobile.jpg"
    alt="An old woman portrait gallery"
  />
</picture>
```

- Setting up configuration for vite to work with [multiple html files](https://vitejs.dev/guide/build.html#multi-page-app):

```js
// vite.config.js
import { defineConfig } from 'vite';
import { resolve } from 'path';

export default defineConfig({
  build: {
    rollupOptions: {
      input: {
        main: resolve(__dirname, "index.html"),
        location: resolve(__dirname, "location/index.html"),
      },
    },
  },
});
```

- And, practicing a lot of layout shifting with CSS Grid...

### Continued development

I'm planning to add [Leaflet JS](https://leafletjs.com/) to the website to make the location page more interactive. Right now, it's using Google Maps `iframe` to display the map.

Migrating to [Astro](https://astro.build/) is also on my to-do list.

If you have any suggestions on how I can improve my code, please [do let me know](https://github.com/dostonnabotov/fem_art-gallery-website/issues)! I'll always look forward to learning new things.

### Useful resources

- [Utopia - Fluid Typography](https://utopia.fyi/type/calculator/) - My go-to website for generating fluid typography.
- [Can I Use](https://caniuse.com/) - For checking browser support for web technologies.
- [Figma](https://www.figma.com/) - For designing the website (*from scratch*).

As for the other resources, I have linked them in the code comments.

## Author

- Website - [Doston Nabotov](https://dostonnabotov.netlify.app)
- Frontend Mentor - [@dostonnabotov](https://www.frontendmentor.io/profile/dostonnabotov)
- Twitter - [@dostonnabotov](https://www.twitter.com/dostonnabotov)

## Acknowledgments

Thanks everyone for helping me become who I am today!
