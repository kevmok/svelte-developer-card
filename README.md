# Customizable developer card built with Svelte

Learning reactivity and logic with Svelte

## Overview

### The Goal

User should be able to:

-   [x] Modify every section on the card through the input boxes
-   [ ] Download the card as an embed to use in your own site

### Demo

[Website Demo](https://svelte-developer-card.vercel.app/)

## Screenshot

![App Screenshot](https://i.imgur.com/6yPoKdB.jpg)

## My process

### Built with

-   Sveltejs/template
-   HTML markup
-   CSS
-   Javascript

### What I learned

-   How to work with spread props
-   Reactive assignments and their bindings
-   #If and #each blocks

Compared to react instead of doing mappings with arrays you can use #each blocks and #if blocks to perform logic in your html markup.

```jsx
// list of objects
const socials = [
        { name: 'twitter', link: 'laura.smith', filename: 'twtr.png' },
        { name: 'facebook', link: 'laura.smith', filename: 'fb.png' },
        {
            name: 'instagram',
            link: 'laura.smith',
            filename: 'ig.png',
        },
        { name: 'linkedin', link: 'smith-laura', filename: 'link.png' },
        { name: 'github', link: 'laura.smith', filename: 'git.png' },
    ];

// Instead of making a label for each object, we can loop over the list like this:
{#each socials as social}
            <label>
                <p>{social.name}:</p>
                <input
                    type="text"
                    placeholder={`${social.name}`}
                    bind:value={social.link}
                />
            </label>
{/each}
```

### Continued development

-   Allow a the user to download the card or make an embed for their own site
-   Adjustments to site responsiveness

## Installation

Clone this repository and install the dependencies...

```bash
  git clone https://github.com/kevmok/svelte-developer-card.git my-app
  cd my-app
  npm install
```

To run locally then start [Rollup](https://rollupjs.org)

```bash
npm run dev
```

## Author

-   Website - [kevinmok.com](https://kevinmok.com)
-   GitHub - [@kevmok](https://www.github.com/Kevmok)
-   Twitter - [@lkBoxer](https://twitter.com/hustlerBoxer)

## Acknowledgements

-   [Scrimba](https://scrimba.com) - I converted your React card to svelte
-   [Svelte](https://svelte.dev/) - For the great tutorial page
