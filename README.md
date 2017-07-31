# SVG Paddleball Game

This is a simple HTML5 game that lets you play paddleball in any current browser.

## Setting Up

Download and copy the text of SVG-Paddleball.html to a text file on your computer. Load it into any web browser (Chrome, Edge, Brave, Vivaldi, Opera, Firefox) and run the file. Some browsers, such as Internet Explorer, may ask for your permission.

## Playing the Game

The object of the game is to move the paddle at the bottom so that it can catch the ball before it hits the ground. If you are playing on a PC or Mac, click to the left or right of the paddle to move it left or right. If you have a touch screen, touch the screen to the left or right of the paddle to move it left or right.

Every time you successfully bounce the ball on the paddle, one point will be added to your score, which will be displayed under the title.

If you miss the ball, the game will end. A dialog will be displayed announcing the game. Click or touch the button to restart the game. Close the browser to end the game.

## Programming Notes

This game uses the SVG DOM, SVG getBBox, requestAnimationFrame, and does not use any external art files.

### SVG DOM

Browsers implementing HTML5 create a Document Object Model (DOM) that allows elements within the web page to be manipulated. One of the features of HTML5 is that you can add SVG (Scalable Vector Graphics) code to your web page and treat it as an extension to the HTML DOM. This lets you access SVG elements as if they were HTML elements.

If you create the SVG element using **createElementNS**, you can work directly with the SVG DOM and bypass the HTML DOM when manipulating SVG elements. Doing so provides speed and efficiency. You must use the data types for SVG elements as outlined in the SVG specification, which follows simple rules.

All current browsers implement the [SVG specification](https://www.w3.org/TR/SVG/). 

### SVG getBBox

**getBBox** is a method that SVG provides to get the bounding box of an object, no matter how complex that object is. A bounding box is defined by the smallest rectangle that can enclose all parts of an object. By getting the bounding boxes of two objects, you can compare the values and determine if there is a collision.

### requestAnimationFrame

This HTML5 method allows a smoother method of animation based on when the browser does a repaint. This ensures that the redrawing will take place without flickering. Browsers generally update their repainting 60 times a second.

Most browsers implement this, but because some browsers used prefixes while implementing this method, prefixes were included.

## Code

Most of the code is based on a simple JavaScript implementation of a ball and paddle. 

### SVG

SVG works with objects. A container object is created with the URL for the W3C SVG implementation. Once the object is created, a board, ball, and paddle are created and added to the container. Depending on the requirements of the element, SVG data types are used, being either strings or numbers.

### CSS

CSS is used to set up the HTML element styles on the page, but CSS styles also can be used with SVG to set properties of the SVG objects.

Code and text copyright (c) 2017 Seth McEvoy

