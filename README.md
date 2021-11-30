# Frontend Mentor - NFT preview card component solution

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
- [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

The challenge was about creating a simple Preview card component using HTML and CSS

### Screenshot

Desktop Mode

![alt text](https://github.com/Salioun/NFT_Preview_Card_Component/blob/main/images/NFT%20Preview%20Card%20Component-%20Desktop.png?raw=true)

Mobile Mode

![alt text](https://github.com/Salioun/NFT_Preview_Card_Component/blob/main/images/NFT_Preview_Card_Component_Mobile.png?raw=true)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Desktop-first workflow


### What I learned

One of my main struggle with this project was the displaying of the eye icon while hovering over the card main image. I tried with the pseudo elements, but I didn't work.
I finally used a ```div``` element in my ``` html``` in order to perform this trick. You can see my code below.

```html
<div class="card-img">
    <div class="hover-image"></div>
    <img src="images/image-equilibrium.jpg" alt="">
</div>
```
```css
.card-img{
    width: 26rem;
    height: 26rem;
    position: relative;
    cursor: pointer;
}

.card-img img{
    width:100%;
    height:100%;
    border-radius: 3%;

}

.card-img .hover-image{
    width: 100%;
    height: 100%;
    background: rgba(0, 255, 247, .7) url("images/icon-view.svg") no-repeat center;
    opacity: 0;
    z-index : 10;
    transition : opacity 0.3s;
    position : absolute;
}

.card-img:hover .hover-image{
    opacity: .7;
}
```

### Continued development

I'll continue to focus on how implement css grid more efficiently. Because I think I'm not so used to this like I thought.

### Useful resources

- [Flex-Box Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - This helped me a lot in my understanding of Flex-boxes


## Author

- Frontend Mentor - [@Salioun](https://www.frontendmentor.io/profile/Salioun)

## Acknowledgments

Credit to Grace on Slack for helping me understand a little more the concept of pseudo-elements