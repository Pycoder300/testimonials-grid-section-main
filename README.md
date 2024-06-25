# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Live demo] (#live demo)
  - [What I learned](#what-i-learned)
  


## Overview
  This challenge involves creating a 4 column, 2 row testimonials grid section using HTML and CSS. The target here is to get as close as possible to the preview image provided in frontend mentor for this challenge. 

### The challenge
  Grid sections are often used in websites to display different content in an ordderly manner. Here i had to create a grid that displays various testimonials of different users. Additionally i had to apply a few different background colors to the grid blocks here. 


## My process
** Please note that the whole process is pretty lengthy so i will only be mentioning the main portions of my approach here** 

  First i created a div tag with a class of grid-container. This div will hold all the grid elements inside it. Now for the subsections of the grid container i made few more div tags and provided them with a class of grid-element. Now some of the grid elements here have different sizes as well as colors so i have given them secondary classes of purple, grey, black, big-white and little-white.
  
  Additionally i have added few more classes inside the HTML document for the h2, p, the top most part of the grid elements containing a profile picture with names and roles. These classes are primary-flex, secondary-flex, header, paragraph, name and role. Primary-flex holds the name and role as its elements, with the display of flex that i have given it. I have provided a flex direction property to it as column so that the name and role stacks on top of each other. Also i have provided an align items property and set it to space between for the gap. 
  
  Now i have put primary-flex inside another class called secondary-flex that will hold it with the circular profile picture as one of its additional elements. I have given a gap of 1rem so that there is a good enough space between the picture and primary-flex. For the font, i have chosen Barlow semi condensed that is available at google fonts. I have styled the header and paragraph classes with their appropriate sizing, opacity, color and font weights in CSS. 

  Now for the grid-container, i have given it a display of grid with four columns and two rows having 1fr (fractional unit). The challenging part here was laying out the individual grid elements inside it so that it looks close enough to the final preview image. One way of doing it was by placing the individual containers to their appropriate location with row and column lines. Now this is a bit more tedious so instead of using this method i went with a different approach. For an easier way of laying out the grid elements, i have added a grid-display-area property and provided a layout value inside double quotion using their class names. (*Although you can provide any values you would like to however i would suggest you to keep it simple with appropriate wordings or names ). So this is how it looks like-

  .grid-container{
      height: 700px; 
      width: 1200px; 
      display: grid; 
      grid-template-columns: 1fr 1fr 1fr 1fr; 
      grid-template-rows: 1fr 1fr; 
      grid-template-areas: 
      "purple purple grey big-white" 
      "little-white black black big-white"; 
      gap: 1.5rem; 
    }

For placing the grid element classes to their respective positions i have added grid-area property to their secondary class with the names as the value which was given to the grid-display-area property of the grid container.
For example: 
.purple{
      grid-area: purple;
    }

For mobile responsiveness i have added a media query having max width of 600px with the following CSS properties inside for the grid container: 

.grid-container{
        width: 350px; 
        grid-template-rows: 2fr 1fr 1fr 1.5fr 2fr; 
        grid-template-columns: 1fr; 
        grid-template-areas:  
        "purple"
        "grey"
        "little-white"
        "black"
        "big-white";
        margin-bottom: 1rem;
      }

As soon as the screen size reduces to 600px or below, you will be able to view this live demo project with all the grid elements stacked on top of each other, so that the content remains visible on narrower screens. 



### Built with
- HTML
- CSS

# View live demo of this project here: 
https://pycoder300.github.io/testimonials-grid-section-main/

### What I learned
grid layout, 
providing columns and rows to grid, 
using grid with @media query for mobile responsiveness.
