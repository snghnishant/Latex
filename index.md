---
layout: default
title: Responsive Web Design
creator: by Nishant Singh
abstract: Responsive web design is the practice of making your website or web application UI look good on different screen sizes and viewport. This can be done using different techniques such as writing media queries for your website, using relative sizing, and so on. Below are the notes on fundamentals of responsive web design and best practices to follow to make your web application and websites look good on devices of different resolutions and display it without breaking the UI. 
---
[Link to Repository](https://github.com/snghnishant/responsive-web-notes)

## Relative Sizing
Using `pixel (px)` for sizing elements in CSS can become a problem when website or webpage is viewed on different screen sizes because it do not auto scales. To overcome this problem we use responsive design by incorporating **relative sizing starts by using units other than pixels**.
1. `em`: It represents size of the base font being used. For example, base font of browser is 16px then `1em = 16px`, `2em = 32px`, `3em = 48px`...
    ```css
    p{
        font-size: 1em;
    }
    ```
2. `rem`: In `<html>` tag, root value is 16px by default. `rem` is used to set a different comparing value for the `font-size` css property for the root element. Advantage of using rem is that all elements are compared to the same font size value making it easy to predict how small or large an element will appear. A css rule can be added as shown below - 
    ```css
    html{
        font-size: 20px; /*Changing default font size to 20px*/
    }
    p{
        font-size: 2rem; /*Since 20px = 1rem, this implies 2rem = 40px*/
    }
    ```
3. `Percentage (%)`: Elements are sized relative to the dimension of their parent element. Look below example -
    ```css
    .main{
        height: 300px;
        width: 500px;
    }
    .main .subsection{
        height: 50%; /*height = 150px*/
        width: 50%; /*width = 250px*/
    }
    ```
    > Note: While attempting 100% height or width for a subsection only be used when content will not have `padding`, `border`, or `margin` otherwise the content might overflow. 
