## Week 1 - The Basics

This week is about leveling the playing field.

There will be some students who find this week slow. But we want to make sure all students are at a basic level before moving on, as this will make the rest of the class go smoothly. Take this time to make sure students understand how the files in their text editor (i.e. Sublime Text, Text Wrangler, etc.) become the web page that is displayed in their browser window.

Joe's About

Joe's Portfolio

* Homework: Finish building your "About" and "Portfolio" pages.


# FEWD - HTML BASICS

### Class 1

---


## Agenda

*	HTML Tags & CSS Selectors Review
*	Structure Reading w/ Understanding
*	External Style Sheets
*	Lab Time

---



## HTML Tags & CSS Selectors Review


---


## HTML Basics

---


## HTML vs HTML5

HTML5 is HTML with a few additions
The Doctype tells you if the page is HTML5 ready.


```<!DOCTYPE html>```


## HTML HISTORY

![HTML History](../../img/unit_1/Timeline_of_web_technologies.jpg)

Note:
image retrieved from http://www.onbile.com/info/wp-content/uploads/2013/09/Timeline-of-web-technologies-639x168.jpg on October 1, 2013.

---


## HTML Syntax

![HTML Syntax](../../img/unit_1/tags.png)

---

## HTML Syntax

![HTML Syntax](../../img/unit_1/tags_attributes.png)

---

## Content Tags

Heading Elements

```<h1>```Largest Heading```</h1>```

```<h2>``` . . . ```</h2>```

```<h3>``` . . . ```</h3>```

```<h4>``` . . .```</h4>```

```<h5>``` . . . ```</h5>```

```<h6>```Smallest Heading```</h6>```

---

## Content Tags

Text Elements

```<p>```This is a paragraph```</p>```

```<code>```This is some computer code```</code>```

---

## Content Tags

Unordered list 
```<ul>``` ```</ul>```

---

## Content Tags

Unordered list item 

	```<li>```First item```</li>```
    ```<li>```Next item```</li>```


---

## Content Tags

links 
 ```<a href="Link">```First item```</a>```


---

Code Along
## General Assembly Press Release

---


## External Style Sheets

---


Exercise
## Cookie Recipe

---

## Homework

*	Create a resume website
*	Watch a video on the Internet about the Internet
*	Read about CSS Colors

---


# FEWD - CSS Basics

### Class 2

---


## Agenda

* HTML & External Style Sheet Review
* Building A Simple Web Page
  * Images
  * Nav
  * Colors
  * Fonts
  * Linking To Other Pages
* Lab Time

---

## HTML Basics Review

---

Exercise
## What Tag Is It?

---

## Building Websites

---

## Images

* Images are placed using the ```<img>``` tag.

```<img src="img/imageName.jpg" alt="alternative text">```

---

## Images

The `img` tag requires a `src` attribute, which tells the browser where to find the image.

---

## Images

How would you write the src?

![](../../img/unit_1/folder_structure.png)

* There are different approaches to specifying an image location

---

## Images

* Inside ```webroot```, a relative path could be used:

#### ```<img src="images/logo.png">```

---

## Images
Relative Path

![Parent Folder Structure](../../img/unit_1/folder_structure_parentDirectory.png)

Note:

* Given this folder structure the same image would be ```<img src="../images/logo.png">```
*
Note that ```..``` means to go up a directory, and can be used repeatedly: `../..` would go up two directories.


---

## Images

Absolute Path

```<img src="/images/logo.png">```

Note:

  Absolute URLs start with a `/`, so if we imagine that our `webroot` directory was stored on a server such that the `webroot/index.html` file is accessible at `http://example.com/index.html`, then placing the logo image could be done from any html page with: ```<img src="/images/logo.png">```

The benefit here is that this same ```src``` path works on any html page, no matter what its location, so the same ```img``` tag can be used on both the ```webroot/index.html``` page and the ```webroot/about/index.html``` page.

The downside is that the path only works if the project is stored to a proper location for serving.


---


## HTML Basics - Images
Full URL

    <img src="https://ga-core.s3.amazonaws.com/production/uploads/program/default_image/397/thumb_User-Experience-Sketching.jpg">

Note:
For linking to images, make sure that you have permission to use the image in this way. Even then, it is often better to host a copy of the same image, rather than link to another server, because it reduces dependency.


---

## HTML Basics - Images

alt attribute

  <img src="puppy.jpg" alt="My cute puppy">

Note:

A piece of text to be used in lieu of the image when the image is unavailable

Using `alt` attributes has the added benefit of giving search engines more linguistic context about the image as it is used on your page.

Reasons an image may not load:

* There was a connection error, the browser didn't download the image.

* The file was not found, perhaps because the image got moved elsewhere and the page wasn't updated yet to reflect the change.

* The user is running a text-based browser such as an older phone with a WAP-style browser, or a non-graphical browser like lynx.

* The user is using a screen reader because she has low vision, which will read the `alt` text aloud or present it through a braille reader.


---

## HTML Basics - Images

There are three main image file formats:

---

## Image File Formats

#### .png

Note:
Supports transparency and semi-transparency, great for logos, icons, and repeating background tiles. Almost always preferable to a `gif`, unless semi-transparency is not needed, and the `gif` format is significantly smaller.


---

## Image File Formats


#### .gif

* Can have basic transparency, typically a `png` is used instead.

---

## Image File Formats

#### .jpeg

Note:
No transparency, can be stored at different compression levels with varying amounts of "lossy-ness", typically the best format for photos. (Try to balance between photo quality and file size.)


---


Code Along
## About Me

---

## CSS

![](../../img/unit_1/css_syntax.png)

---


## CSS

Where does CSS go?

* Inline
* In the `head`
* In a separate file


Note:
CSS should go in a separate file. We're going to start by placing them in the head for convenience and to learn the syntax. We'll show inline styles at the end, just to demonstrate.


---

## CSS

Using a separate CSS file

Its best practice to put CSS in its own file and link to it from the `<head>`.

```<link rel="stylesheet" href="style.css">```

Note:
"The `link` tag needs two attributes: `rel="stylesheet"` and an `href` attribute.

The `href` attribute value works very similarly to linking to an image, or to another page.


---

## CSS Break Down

```
p {
  color: red;
  font-weight: bold;
}
```
---

## CSS Break Down

This whole thing is called a **rule**.

The `p` is called a **selector**, and it's followed by a set of **declarations** in a **declaration block**.

---

## CSS Break Down

The **selector**, `p` in this case, specifies what parts of the HTML document should be styled by the declaration. This selector will style all `p` elements on the page.

---

## CSS Break Down

The **declaration block** here is:

```
{
  color: red;
  font-weight: bold;
}
```

**Declarations** go inside curly braces.

---


## CSS Break Down

#### Declarations

This example has two declarations. Here's the first:

```
color: red;
```

Note:
Every declaration is a **property** followed by a **value**, separated by a colon, ending in a semicolon.

In this declaration, we are setting the `color` **property** to the **value** `red`.


---


## CSS Break Down

Let's look at the second declaration:

```
font-weight: bold;
```

Note:

What style **property** are we specifying here?

What **value** are we setting that **property** to?

Try writing a new set of styles for another element, like an `h1`.


---

## CSS Break Down

Why might we want to link to a separate CSS file?

Note:

Discuss as a class


---

## Cascading Style Sheets (CSS)
### Colors

Colors can be specified in CSS in a variety of ways:

![](../../img/unit_1/color.png)

Note:
* keyword
* hex codes
* rgb
* hsl
* rgba
* hsla


---

## Color
### Color Keywords

These are used less frequently, but are handy for basic colors like `black` and `white`. There are several

See [here](http://msdn.microsoft.com/en-us/library/ie/aa358802.aspx) for more

---

## Color
### Hex Codes (RGB)

![Hex Color explanation](../../img/unit_1/hex_colors.png)

Note:
"Hex" values are so-called because they use hexadecimal, or base-16, to describe the color values for red, green, and blue. Each of the 3 color values is expressed by two hexadecimal digits, from `00` (no color) to `FF` (full color), and are written in the order red, green, then blue, after an initial `#` sign.

Hex values can be abbreviated to only 3 digits if each digits is doubled. So `#FFFFFF` (white) can be expressed more succinctly as `#FFF`, and `#000000` (black) can be expressed as `#000`. `#FA6198`, however, cannot be abbreviated without altering the color.


---

## Color
### RGB Color Values

#### ```rgb(0,0,0)```

* The first value is red, the second green, the third blue.

* Each value can range from 0 to 255, which expresses the same number of color steps as 00 to FF in base-16.


Note:
FF in base-16 is equivalent to 255 in base-10.

In RGB, `rgb(0,0,0)` is black, `rgb(255,255,255)` is white, `rgb(255,0,0)` is red, etc.

White-space is allowed *inside* the parentheses, so `rgb(255, 0, 0)` will do just as well.

---

## Color
### RGBa Colors


* RGBa works identically to RGB, expect that it takes a 4th value called the "alpha".
* This is a value between 0 and 1 which will be used to determine a color's opacity on the page,


![](../../img/unit_1/rgba_color.png)

Note:
0 is completely transparent, and 1 being solid. 0.5 or .5 is 50% opacity.

Thus, __rgba(0,0,0,.25)__ is black at 25% opacity and __rgba(255, 255, 255, 0.8)__ is white at 80% opacity.

The alpha value can be in decimal form but cannot use a percentage. When a decimal is used, the leading zero is optional.

---

## Color
### HSL Colors

#### HSL
* Similar notation to RGB values, but specify colors using hue, saturation, and lightness.


#### HSLa
* As with RGBa, HSLa is exactly like HSL for the first 3 values, but takes a 4th alpha-channel value.

Note:
**Hue** is expressed as a degree angle measure, with red being at 0, green at 120, and blue at 240. Note that the degree unit is implied, and that the angle wraps around, so 360 also refers to red, and -120 is the same as 240 (blue).

**Saturation** is expressed as a percentage, with 100% being a fully saturated color, and 0% being a shade of gray (no hue).

**Lightness** is also expressed as a percentage, 0% being black, and 100% being white. 50% lightness is the "normal" color range: anything above 50% gives a white tint, anything below 50% gives a black shade.

As an example, red is ```hsl(0, 100%, 50%)```, which is equivalent to ```#FF0000```.

Note that changing the opacity allows whatever colors are "behind" an element to shine through, which can alter the visible color significantly, especially at lower opacities.


---


## CSS
### Review

Add a couple points here with the major takeaways for the basics of CSS.


---


Exercise
## Lab Time
* Your Portfolio!

---

### Week 2 Advanced CSS

This week is about more complex CSS topics, including floats and positioning elements on the page in addition to creating DIVs and differentiating between classes and IDs.


__Main project and homework:__ Relaxr Landing Page. This web project has 2 parts. This week start building a single column layout.


# FEWD - Box Model & More CSS

### Class 3

---


## Agenda

* Review
* Box Model
* Nested Selectors
* HTML Template
* Lab Time
  * How To Start

---

## Review

What do students need help with?

---

## Box Model

Every element in web design is a box.

---


## Box Model

![](http://www.mandalatv.net/itp/drivebys/css/lib/img/box_model.gif)

---

## Box Model

### Width = width + padding-left + padding-right + border-left + border-right

### Height = height + padding-top + padding-bottom + border-top + border-bottom

---


Code Along
## Tags & Boxes

---


Exercise
## Draw Me a DOM

---

Code Along
## Nested Selectors

---


Exercise
## Relaxr Landing Page

---

# FEWD - Layout

### Class 4

---


## Agenda

* Review
* Divs, Classes and IDs
* HTML5 Structural Elements
* Floats
* Lab Time

---

## Review

What would you like to review?

---

## Div

What is a Div?

---


## class & id

With classes and ids we can target specific elements on a page, so we can manipulate it uniquely.

---

## class & id

![](../../img/unit_1/tags_attributes.png)

---


Code Along
## class & id

---

## class & id

#### IDs are unique

#### Classes are not unique

---

## class & id

When should you use them?

---

## class & id

How to __select__ classes in CSS

```
.className
```

```
# idName
```

---

## HTML5 Structural Elements

Adding structure to HTML elements that are related to content layout.

* header
* aside
* footer

---


## Floats

Float is a CSS positioning property, used to layout a web page.

![](http://css-tricks.com/wp-content/csstricks-uploads/web-layout.png)

Note:
Image from Chris Coyier's CSS-Tricks

---

Code Along
## Floating Sections

---


Lab
## Layout Challenge

---

### Week 3 HTML/CSS Lab

This week we continue to teach students how to think like a Front-End Web Developer. The next to lessons are dedicated to in class lab time, where students practice and review HTML/CSS.


__Main projects and homeworks:__ Relaxr Part 2 & Startup Match Maker.

## Lesson 05 - Layout Lab


### LEARNING OBJECTIVES

* Apply floats and clearing techniques to effectively create a two column layout.

<br>

---

**Note:** Starter/Solution code for this lesson is located in the Week 3 [Assignment directory](../Assignment)


### SCHEDULE


| Time        | Topic| GA Suggested| Comments |
| ------------- |:-------------|:-------------------|:----------------|
| _30 min_ | Floats and Clears Review |  | |
| _20 min_ | [How To Start](#how-to-start)| Div' Up The Content | Show students how and where to start. During lab time we will give students a png they will reproduce using HTML and CSS. |
| _120 min_ | [Lab Time](#lab-time) | Relaxr_Blog part 2 | Students add more complex elements and styling to the Fashion blog.|


---

### LESSON PLANNING NOTES

Below you will find notes on each section from the proposed schedule above. These notes are  meant to help you plan for a great class.

<a name=how-to-start>
#### How To Start
_Time: 20min_

* This is an opportunity to show students how to start the assignment. Last class students practiced layouts using boxes. Now student apply the same technique to create a two coloumn layout for the Fashion Blog.


| Discussion | 'Div' Up the Content|
| ------------- |:-------------|
| __Time__ | 10 min |
| __Topics__ | Identifying content sections (divs, classes, ids) |
| __Description__ | As a class determine what divs, classes and ids are required for Relaxr's blog. |
| __Notes__ | Ask students to get into groups and draw the outline (layout) of the Relaxr's blog. When complete if should like a series of boxes much like the layout challenge. As a group they can determine what elements on the page have similar styling. Share answers of how the site should be sectioned. This will be the starting point of the course. |

<a name=lab-time>
#### Lab Time
_Time: 120min_


#### [Relaxr Blog]()

|Exercise | [Relaxr Part 2](../Assignment/README.md)|
|:------------- |:-------------|
| __Time__ | 45 min |
| __Topics__ | planning and building a website. |
| __Description__| Students add more styles and content to the Relaxr blog |
| __Notes__| Make sure students know the content sections and structural elements needed to complete the exercise. Encourage students to plan before they begin coding. We want them to be thoughtful about what they are doing and how they are approaching the exercise. |


Note: The starter and solution code for this lab will be found in the [assignment file](../Assignment/README.md) as students will be asked to finish this for homework - be sure to point that out! Also, encourage students to take a shot at the bonus - link all of their Relaxr pages and enable a JavaScript alert.

---


No slides for this lesson

## Lesson 06 - Lab Session


### LEARNING OBJECTIVES

* Practice web development by transforming a design comp into an HTML and CSS web page.


### SCHEDULE

| Time        | Topic| GA ICLs| Comments |
| ------------- |:-------------|:-------------------|:----------------|
| _180 min_ | [Lab Session]() | Startup Match Maker | Students build a site with little guidance on how to start. |


---


### LESSON PLANNING NOTES

Below you will find notes on each section from the proposed schedule above. These notes are  meant to help you plan for a great class.

#### Lab Time
_Time: 180min_

* A little less hand holding this time. Students should have an idea of how to start this time.


| Exercise | [Startup Matchmaker](starter_code)|
|:------------- |:-------------|
| __Time__ | 180 min |
| __Topics__ | html, css, planning |
| __Description__| Students work in groups to determine what needs to be done. They then code the website.  |
| __Notes__ |This is an ambitious site to build in week 3. The goal is to encourage students to divide and conquer. We want to teach them how to look at a png file determine the sections that are needed and then code.|


__Please note that students will need to Google:__

* background-image
* ```<del>``` ```<ins>```
* overflow

---



