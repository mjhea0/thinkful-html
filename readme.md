Developed in conjunction with [Thinkful](http://thinkful.com).

![thinkful](https://raw.github.com/mjhea0/thinkful-html/master/logo.png)

Come code along with me! Sign up [here](http://www.thinkful.com/a/mentorship-preview).

<hr>

# Introduction to HTML and CSS

Websites are made up of many things, but HTML (Hyper Text Markup Language) and CSS (Cascading Style Sheets) are two of the most important components. Together, they are the building blocks for every single webpage on the Internet.

Think of a car. It, too, is made up of many attributes. Doors. Windows. Tires. Seats. In the world of HTML, these are the `elements` of a webpage. Meanwhile, each of the car's attributes are usually different. Perhaps they differ by size. Or color. Or wear and tear. These attributes are used to define how the `elements` look. Back in the world of webpages, CSS is used to define the look and feel of a webpage.

Now let's turn to an actual web page ..

## Requirements

Before we start, you need a *source code editor*, which is simply a text editor designed specifically for writing source code. Some popular editors include Notepad++ (Windows), TextMate (Mac), and Gedit (cross-platform). For this exercise, please download the cross-platform editor [Sublime Text](http://www.sublimetext.com/2), which is an editor designed for simplicity and ease of use.

Also, please make sure you have [Google Chrome](http://google.com/chrome) installed.

## HTML

HTML gives a web pages structure, allowing you to view it from a web browser:

Start by adding some basic structure:

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

Copy and paste this basic webpage structure into your text editor. Save this file as *index.html*.

This structure is commonly referred to as a boilerplate template. Such templates are used to speed up development so you don't have to code the features common to every single webpage each time you create a new page. Most boilerplates include more features (or boilerplate code), but let's start with the basics.

### What's going on?

1. The first line, `<!DOCTYPE html>` is the document type declaration, which tells the browser the version of HTML the page is using (HTML5, in our case). Without this, browsers can get confused, especially older versions of Internet Explorer. 
2. `<html>` is the first tag and it informs the browser that all code between the opening and closing, `</html>`, tags is HTML. 
3. The `<head>` tag contains links to CSS stylesheets and Javascript files that we wish to use in our web page, as well as meta information used by search engines for classification. In the above HTML, I used the `<title>` tag to give the web page a title.
4. All code that falls within the `<body>` tags are part of the main content of the page, which will appear in the browser to the end user.

This is how a standard HTML page is structured.

Let's add four tags:

1. title `<title>`
2. heading `<h1>`
3. img `<img>`
4. break `<br>`


```html
<!DOCTYPE html>
<html>
  <head>
  	<title>My bumblebee website</title>
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
  </body>
</html>
```

Open the page in Chrome; it should look like this:

![html](/images/index1.png)


### Elements, Tags, and Attributes

1. Tags form the structure of your page. They surround and apply *meaning* to content. There usually is an opening tag and then a closing tag, like - `<div></div>`, a divider. Again, we are using the following tags:
  - Title: `<title>` displays the title in the browser toolbar. It's also used for the title when its added to your browser's favorites and the title of your page for search engine results.
  - Headings: These include the `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` and `<h6>` tags. `<h1>` is the main heading and the remaining headings decrease in size, with `<h6>` being the smallest. It's best practice to use the `<h1>` tag once per page, while the other tags can be used any number of times, but they should always be in order. In other words, `<h3>` should be a sub-heading of `<h2>` and `<h4>` should be a sub-heading of `<h3>`. Can you recognize the header in the HTML. 
  - Some tags, like the `<img>` (image) and `<br>` (line break) tags do not require a closing tag. Notice how I included one `<br>` tag with a `/` on the end. This was a best practice in previous versions of HTML. HTML5, on the other hand - the version we are using - is much more relaxed and does not require a `/`, but it will work fine with it as well. It's really the developer's preference.
2. Elements represent the tags as well as whatever falls between the opening and closing tags, like - `<title>My bumblebee website</title>`
3. Attributes (sometimes referred to as selectors) are used to select the tag for some purpose. In our case we are going to use them for defining styles, when we get to CSS. Selectors in most cases are either `id`s or `class`es. In the above example, notice the id `my-header`, which is associated with the `<h1>` tag. We'll look more at this later. Further, we also use the attributes `width="240"` and  `height="180"`. These are defined using attributes directly within the HTML, or you can also place them in the CSS stylesheet. Again, more on this later.


### Additional Tags

Two additional tags are lists (ordered `<ol>` and unordered `<ul>`) as well as links `<a href>`. Look these up on your own. Mozilla has an excellent reference guide [here](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/HTML5_element_list).

### Putting it all together

Let's add all the tags that were discussed.

#### Headings

```html
<h2>Wonder, wonderful bumblebees</h2>
<h2>About the Bumblebee</h2>
<h2>Types of Bees:</h2>
<h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My bumblebee website</title>
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <h2>Wonder, wonderful bumblebees</h2>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
    <h2>About the Bumblebee</h2>
      <h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
    <br>
    <h2>Types of Bees:</h2>
  </body>
</html>
```

#### Paragraph

Paragraphs: The `<p>` tag is used for splitting content literally into separate paragraphs. Each new `<p>` tag will appear on a new line.

```html
<p>A bumblebee is any member of the bee genus Bombus, in the family Apidae. There are over 250 known species, existing primarily in the Northern Hemisphere although they also occur in South America. They have been introduced to New Zealand and the Australian state of Tasmania.</p>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My bumblebee website</title>
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <h2>Wonder, wonderful bumblebees</h2>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
    <h2>About the Bumblebee</h2>
      <h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
      <p>A bumblebee is any member of the bee genus Bombus, in the family Apidae. There are over 250 known species, existing primarily in the Northern Hemisphere although they also occur in South America. They have been introduced to New Zealand and the Australian state of Tasmania.</p>
    <br>
    <h2>Types of Bees:</h2>
  </body>
</html>
```

#### Ordered Lists

```html
<ol>
  <li>Southern plains bumblebee</li>
  <li>New garden bumblebee</li>
  <li>Early bumblebee</li>
  <li>Orange-belted bumblebee</li>
  <li>Buff-tailed bumblebee or large earth bumblebee</li>
</ol>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My bumblebee website</title>
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <h2>Wonder, wonderful bumblebees</h2>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
    <h2>About the Bumblebee</h2>
      <h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
      <p>A bumblebee is any member of the bee genus Bombus, in the family Apidae. There are over 250 known species, existing primarily in the Northern Hemisphere although they also occur in South America. They have been introduced to New Zealand and the Australian state of Tasmania.</p>
    <br>
    <h2>Types of Bees:</h2>
      <ol>
        <li>Southern plains bumblebee</li>
        <li>New garden bumblebee</li>
        <li>Early bumblebee</li>
        <li>Orange-belted bumblebee</li>
        <li>Buff-tailed bumblebee or large earth bumblebee</li>
      </ol>
  </body>
</html>
```

Check it out in your browser. Add some more elements, or let's move on to CSS so we can make the site look better.

On to CSS ..

## CSS

While HTML provides, structure, CSS is used for styling, making webpages look nice. From the size of the text to the background colors to the positioning of HTML elements, CSS gives you control over almost every visual aspect of a page.


CSS and HTML work in tandem. CSS styles (or rules) are applied directly to HTML elements. For example, remember this element from above - `<h1 id="my-header">Bees!</h1>`. Well, since there is an `id` selector associated with it, we can assign CSS styles to it using an external stylesheet.

```css
#my-header {
  color: #660000;
}
```

**Save this as "styles.css".**

> There are three ways that you can assign styles to HTML tags. Inline. Internal. Or External. Inline styles are placed directly in the tag; these should be avoided, though, as it's best practice to keep HTML and CSS styles separated (don't mix structure with presentation!). Internal styles fall within the head of a website. Again, these should be avoided as well due to reasons mentioned before. Read more about this [here](http://www.w3schools.com/css/css_howto.asp).

Next, we need to "link" our HTML page and CSS stylesheet. To do so, add the following code to the `<head>` section of the HTML page just below the title:

```html
<link rel="stylesheet" href="styles.css">
```

Your code should now look like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My bumblebee website</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <h2>Wonder, wonderful bumblebees</h2>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
    <h2>About the Bumblebee</h2>
      <h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
      <p>A bumblebee is any member of the bee genus Bombus, in the family Apidae. There are over 250 known species, existing primarily in the Northern Hemisphere although they also occur in South America. They have been introduced to New Zealand and the Australian state of Tasmania.</p>
    <br>
    <h2>Types of Bees:</h2>
      <ol>
        <li>Southern plains bumblebee</li>
        <li>New garden bumblebee</li>
        <li>Early bumblebee</li>
        <li>Orange-belted bumblebee</li>
        <li>Buff-tailed bumblebee or large earth bumblebee</li>
      </ol>
  </body>
</html>
```

Save the file. Check it out in your browser.

See the difference? Yes, it's subtle - but the `<h1>`, or main header, is a maroon color.

You can change certain elements even if they are not *explicitly* found within the HTML of the page, like the background color.

Update your CSS file:

```css
body {
  background-color: #FFFF00
}

#my-header {
  color: #660000;
}
```

Save. Refresh.

### What's going on?

Look back at the CSS file.

1. We have the `#my-header` *selector*, which is associated with the selector in our HTML document, followed by curly braces.
2. Inside the curly braces, we have *properties*, which are descriptive words, like font-weight, font-size, or background color. In our case, we have `color`.
3. *Values* are then assigned to each property, which are preceded by a colon and followed by a semi-colon. [http://cssvalues.com/](http://cssvalues.com/) is an excellent resource for finding the acceptable values given a CSS property. I use this almost everyday.

Can you figure out what's going on with the `body` tag?

### Additional Properties

You can view all the available properties [here](http://www.w3.org/TR/CSS2/propidx.html). Pay attention to the font-related properties - like font-family, font-weight, and font-style - as you will be using these later.

Margins, padding, and borders are also good properties to go over since they appear in almost every web page.

### Putting it all together

1. First, add some selectors to the HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My bumblebee website</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1 id="my-header">Bees!</h1>
    <h2>Wonder, wonderful bumblebees</h2>
    <p>
      <br/>
      <img src="http://farm4.staticflickr.com/3775/12059206813_e37135c9cf_z.jpg" width="240" height="180"/>
      <br>
    </p>
    <h2>About the Bumblebee</h2>
      <h3>(From <a href="http://en.wikipedia.org/wiki/Bumblebee">Wikipedia)</a></h3>
      <p id="first-paragraph">A bumblebee is any member of the bee genus Bombus, in the family Apidae. There are over 250 known species, existing primarily in the Northern Hemisphere although they also occur in South America. They have been introduced to New Zealand and the Australian state of Tasmania.</p>
    <br>
    <h2>Types of Bees:</h2>
      <ol>
        <li class="odd">Southern plains bumblebee</li>
        <li class="even">New garden bumblebee</li>
        <li class="odd">Early bumblebee</li>
        <li class="even">Orange-belted bumblebee</li>
        <li class="odd">Buff-tailed bumblebee or large earth bumblebee</li>
      </ol>
  </body>
</html>
```

Now, let's update the CSS file.

```html
/* this is a comment */

body {
  font-family: arial, helvetica, sans-serif;
  background-color: #FFFF00;
  max-width: 500px;
  text-align: center;
}

p {
  line-height: 20px;
}

h1 {
  font-style: italic;
  text-transform: uppercase;
}

#my-header {
  color: #660000;
}

#first-paragraph {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #000000;
}


.even {
 font-style: italic;
}

.odd {
  color: red;
}
```

Save. Refresh your browser.

What do you think? Good. Bad. Ugly? Change the color of the background and header on your end. The [color picker](http://color.hailpixel.com/) is nice for finding colors. [Update](http://www.flickr.com/) the picture, too, if you want. 

## Your turn!

While I provide a brief review, work along with me to develop your own basic site. 

1. Create a basic HTML page with the doctype, html, head, and body tags
2. Add a header (H1)
3. Create an order list
4. Add an external CSS file (make sure to link to the HTML page)
4. Change the background color and font size
4. Style the list

Show it off!

## Chrome Developer Tools

Using Chrome Developer Tools, we can not only view how someone added, for example, a CSS selector to make the HTML text to appear to hoover - but it's also an excellent means of testing either HTML or CSS changes directly from the browser. This can save a lot time

Open up the HTML page we worked on. Right Click on the first paragraph. Select "Inspect Element". Notice the styles on the right side of the Developer Tools pane associated with the paragraph. Do you see the styles associated with the first paragraph? Go ahead and change the size of the border from 2px to 20px: 

![html](/images/devtools.png)

Change the color of the even rows from black to something super cool.

You can also edit your HTML in real time. With Dev Tools open, right click the text and select "Edit as HTML"

> Be careful as these changes are temporary. Watch what happens when you refresh the page.

## Extra Credit

1. Try some of [these](http://en.wikiversity.org/wiki/Web_Design/HTML_Challenges) challenges.
