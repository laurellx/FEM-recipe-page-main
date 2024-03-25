# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### Screenshot

![Mobile](/assets/images/solution/Mobile.png)
![Desktop](/assets/images/solution/Desktop.png)

### Links

- Solution URL: [GitHub](https://github.com/laurellx/FEM-recipe-page-main)
- Live Site URL: [Vercel](fem-recipe-page-main.vercel.app)

## My process

To create this project I started from editing the HTML file organising it from a semantic point of view, using the section and article tags, along with the header, main and footer ones. I took into account the fact that there is a main difference between the mobile and desktop version: there is an additional background that is not visible on the mobile version. Nonetheless, I did create the mobile view first and proceeded, then, to wrap the whole content within a main div, inserted within the body tags.
I worked with SASS because I want to become more and more familiar with it: all its features permit to avoid repeating code and, although I am confident I could have saved some more, I think the variables and mixins already helped with potential code repetitions.
Once I was satisfied with the view of the mobile version, I created the mixin to make the project responsive, with the corresponding variables for breakpoints.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- SASS
- Mobile-first workflow

### What I learned

The mixins section of the styles is probably the most interesting of the project, as I created a few of them to avoid code repetition and, also, to make the project responsive. I confess this is some recycled code from my [previous FEM project](https://www.frontendmentor.io/solutions/mobilefirst-solution-using-sass-t9tbtCPBCZ)

```css
@mixin separator {
  content: "";
  display: block;
  background-color: $separator;
  height: 1px;
  width: 100%;
}
```

Another one from the CSS (SASS) part, some piece of code that might be considered interesting is related to the list items and the indentation from the bullet point.

```css
li {
  padding: 5px 15px;
  list-style-type: decimal;
  line-height: 22px;
  @include paragraph;
  &::marker {
    color: $sectionText;
    font-weight: bold;
  }
}
```

### Useful resources

- [CSS-Tricks](https://css-tricks.com/everything-you-need-to-know-about-the-gap-after-the-list-marker/) - This page has been extremely useful with the tricky bullet points of the ordered and unordered lists in CSS; it provides a useful tool to visualize how to increase/reduce indentation of the lists and, even more interesting, how to increase/reduce the space between the list bullet point and the text of the item.
- [Stack Overflow](https://stackoverflow.com/questions/1257430/how-can-i-apply-a-border-only-inside-a-table) - One of the solutions proposed in this article helped me to style the html table at the bottom of the webpage; I must say I do not usually utilise html tables and it was very useful to understand how the table tags work.

## Author

- Frontend Mentor - [@laurellx](https://www.frontendmentor.io/profile/laurellx)
- GitHub - [@laurellx](https://github.com/laurellx)

## Acknowledgments

Thanks to all the people that made the same Google searches as me and allowed me to find the answer to all my CSS and HTML questions online. Also thanks to the OSOM House coffee place in Madrid that hosted me during the creation of this project: it has been quite an easy challenge, but finding the motivation to code on a beautiful Spring Saturday is not, and the amazing coffee I had here truly helped.
And thanks to myself for paying for it.
