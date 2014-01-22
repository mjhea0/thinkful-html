# Introduction to HTML and CSS

Websites are made up of many things, but HTML (Hyper Text Markup Language) and CSS (Cascading Style Sheets) are two of the most important components. Together, they are the building blocks for every single webpage on the Internet.

Think of a car. It, too, is made up of many attributes. Doors. Windows. Tires. Seats. In the world of HTML, these are the `elements` of a webpage. Meanwhile, each of the car's attrubutes are usually different. Perhaps they differ by size. Or color. Or wear and tear. These attributes are used to define how the `elements` look. Back in the world of webpages, CSS is used to define the look and feel of a webpage.

Now let's turn to an actual web page ..

## Requirements

Before we start, you need a *source code editor*, which is simply a text editor designed specifically for writing source code. Some popular editors include Notepade++ (Windows), TextMate (Mac), and Gedit (cross-platform). For this exercise, please download the cross-platform editor [Sublime Text](http://www.sublimetext.com/2), which is an open-source editor designed for simplicity and ease of use.

Also, please make sure you have [Google Chrome](http://google.com/chrome) installed.

## HTML

HTML gives a web pages structure, allowing you to view it from a web browser:

```html
<html>
  <head>
  	<title>My bumblebee website</title>
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <p>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg"/>
    </p>
  </body>
</html>
```

**Let's look at some of the elements in this simple example ..**

1. Tags form the structure of your page. There usually is an opening tag and then a closing tag, like - `<div></div>`. Some tags, like the `<img>` tag does not require a closing tag. It's best practice to add a `/` on the end of such tags.
2. Elements represent the tags as well as whatever falls within the tags, like - `<h1>Hello, World!</h1>`
3. Selectors are used to select the tag for some purpose. In our case we are going to use them for defining styles. Selectors are either `id`s or `class`es. In the above example, notice the id `my-header`, which is associated with the `<img>` tag.

If you open the page in Chrome, it should look like this:

![page1](page1.png)

Boring! Let's make this look a bit better.

On to CSS ..

## CSS

While HTML provides, structure, CSS is used for styling, making webpages look nice. From the size of the text to the background colors to the positionging of HTML elements, CSS gives you control over almost every visual aspect of a page.


CSS and HTML work in tandem. CSS styles (or rules) are applied directly to HTML elements. For example:



## Your turn!

1. Add a header (H1)
2. Create an order list
3. Change the background color and font size
4. Style the list


## Inspecting a Web Site

Chrome Developer Tools

## Extra Credit
