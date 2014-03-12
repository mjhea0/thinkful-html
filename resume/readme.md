# Creating an Online Resume: An Introduction to HTML and CSS

![resume](https://raw.github.com/mjhea0/thinkful-html/master/resume/images/resume2.png)

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
3. paragraph `<p>`
4. img `<img>`
5. break `<br>`


```html
<!DOCTYPE html>
<html>
  <head>
    <title>Resume: Darth Vader, Lord of the Sith</title>
  </head>
  <body>
    <h1 id="heading">Darth Vader</h1>
    <p>Lord of the Sith</p>
    <br/>
    <img src="http://upload.wikimedia.org/wikipedia/en/7/76/Darth_Vader.jpg">
    <br>
  </body>
</html>
```

Open the page in Chrome; it should look like this:

![resume1](https://raw.github.com/mjhea0/thinkful-html/master/resume/images/resume1.png)


### Elements, Tags, and Attributes

1. Tags form the structure of your page. They surround and apply *meaning* to content. There usually is an opening tag and then a closing tag, like - `<div></div>`, a divider. Again, we are using the following tags:
  - Title: `<title>` displays the title in the browser toolbar. It's also used for the title when its added to your browser's favorites and the title of your page for search engine results.
  - Headings: These include the `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` and `<h6>` tags. `<h1>` is the main heading and the remaining headings decrease in size, with `<h6>` being the smallest. It's best practice to use the `<h1>` tag once per page, while the other tags can be used any number of times, but they should always be in order. In other words, `<h3>` should be a sub-heading of `<h2>` and `<h4>` should be a sub-heading of `<h3>`. Can you recognize the header in the HTML. 
  - Some tags, like the `<img>` (image) and `<br>` (line break) tags do not require a closing tag. Notice how I included one `<br>` tag with a `/` on the end. This was a best practice in previous versions of HTML. HTML5, on the other hand - the version we are using - is much more relaxed and does not require a `/`, but it will work fine with it as well. It's really the developer's preference.
2. Elements represent the tags as well as whatever falls between the opening and closing tags, like - `<title>Resume: Darth Vader, Lord of the Sith</title>`
3. Attributes (sometimes referred to as selectors) are used to select the tag for some purpose. In our case we are going to use them for defining styles, when we get to CSS. Selectors in most cases are either `id`s or `class`es. In the above example, notice the id `header`, which is associated with the `<h1>` tag. We'll look more at this later.

### Additional Tags

Two additional tags are lists (ordered `<ol>` and unordered `<ul>`) as well as links `<a href>`. Look these up on your own. Mozilla has an excellent reference guide [here](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/HTML5_element_list).

### Putting it all together

Let's add all the tags that were discussed.

#### Headings

```html
<h2>History and Profile</h2>
<h2>Education</h2>
<h2>Work History</h2>
<h2>Skillset</h2>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Resume: Darth Vader, Lord of the Sith</title>
  </head>
  <body>
    <h1 id="heading">Darth Vader</h1>
    <p>Lord of the Sith</p>
    <br/>
    <img src="http://upload.wikimedia.org/wikipedia/en/7/76/Darth_Vader.jpg">
    <br>
    <h2>History and Profile</h2>
    <h2>Education</h2>
    <h2>Work History</h2>
    <h2>Skillset</h2>
  </body>
</html>
```

#### Paragraph

Paragraphs: The `<p>` tag is used for splitting content literally into separate paragraphs. Each new `<p>` tag will appear on a new line.

```html
<p>I am a fearsome cyborg with extensive experience gained as the supreme commander of the Galactic Empire. I successfully delivered the largest strategic initiative within the Star Wars universe, working in partnership with Emperor Palpatine and other key stakeholders to bring the project in on time and within budget, twice because of that cursed rebellion. With a powerful bass voice, imposing body armour and signature respiratory breathing, I am able to use my influence at all levels, whether leading Imperial subordinates, devastating estranged family members, or crushing the Rebel Alliance.</p>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Resume: Darth Vader, Lord of the Sith</title>
  </head>
  <body>
    <h1 id="heading">Darth Vader</h1>
    <p>Lord of the Sith</p>
    <br/>
    <img src="http://upload.wikimedia.org/wikipedia/en/7/76/Darth_Vader.jpg">
    <br>
    <h2>History and Profile</h2>
    <p>I am a fearsome cyborg with extensive experience gained as the supreme commander of the Galactic Empire. I successfully delivered the largest strategic initiative within the Star Wars universe, working in partnership with Emperor Palpatine and other key stakeholders to bring the project in on time and within budget, twice because of that cursed rebellion. With a powerful bass voice, imposing body armor and signature respiratory breathing, I am able to use my influence at all levels, whether leading Imperial subordinates, devastating estranged family members, or crushing the Rebel Alliance.</p>
    <h2>Education</h2>
    <h2>Work History</h2>
    <h2>Skillset</h2>
  </body>
</html>
```

#### Unordered Lists

```html
<ul>
  <li>Imperial Palace, 000-001</li>
  <li>Hololink: 655321-666</li>
  <li>lordvader@gmail.com</li>
</ul>
```

and

```html
<ul>
  <li>Jedi Academy, Master warrior-monk and basket weaving</li>
  <li>Obi-Wan Kenobi School of Training, Jedi Training</li>
</ul>
```

and

```html
<ul>
  <li>His Excellency Palpatine I, Emperor of the Galaxy - Major General</li>
  <li>The Jedi Order - Liaison to the Supreme Chancellor</li>
  <li>Watto's Junk Dealership - electronics repair</li>
</ul>
```

and

```html
<ul>
  <li>Oppressing the Galaxy</li>
  <li>Great Physical Strength</li>
  <li>Mastery of the Force</li>
  <li>Lightsaber Duels</li>
  <li>Team Leadership</li>
  <li>Imperial Weapons Research</li>
  <li>Ruby Scripting Ninja</li>
  <li>Master pick-pocketter</li>
</ul>
```

Updated code:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Resume: Darth Vader, Lord of the Sith</title>
  </head>
  <body>
    <h1 id="heading">Darth Vader</h1>
    <p>Lord of the Sith</p>
    <ul>
      <li>Imperial Palace, 000-001</li>
      <li>Hololink: 655321-666</li>
      <li>lordvader@gmail.com</li>
    </ul>
    <br/>
    <img src="http://upload.wikimedia.org/wikipedia/en/7/76/Darth_Vader.jpg">
    <br>
    <h2>History and Profile</h2>
    <p>I am a fearsome cyborg with extensive experience gained as the supreme commander of the Galactic Empire. I successfully delivered the largest strategic initiative within the Star Wars universe, working in partnership with Emperor Palpatine and other key stakeholders to bring the project in on time and within budget, twice because of that cursed rebellion. With a powerful bass voice, imposing body armour and signature respiratory breathing, I am able to use my influence at all levels, whether leading Imperial subordinates, devastating estranged family members, or crushing the Rebel Alliance.</p>
    <h2>Education</h2>
    <ul>
      <li>Jedi Academy, Master warrior-monk and basket weaving</li>
      <li>Obi-Wan Kenobi School of Training, Jedi Training</li>
    </ul>
    <h2>Work History</h2>
    <ul>
      <li>His Excellency Palpatine I, Emperor of the Galaxy - Major General</li>
      <li>The Jedi Order - Liaison to the Supreme Chancellor</li>
      <li>Watto's Junk Dealership - electronics repair</li>
    </ul>
    <h2>Skillset</h2>
    <ul>
      <li>Oppressing the Galaxy</li>
      <li>Great Physical Strength</li>
      <li>Mastery of the Force</li>
      <li>Lightsaber Duels</li>
      <li>Team Leadership</li>
      <li>Imperial Weapons Research</li>
      <li>Ruby Scripting Ninja</li>
      <li>Master pick-pocketter</li>
    </ul>
  </body>
</html>
```

Check it out in your browser. Add some more elements. Or: jump right to CSS ...


## CSS

While HTML provides, structure, CSS is used for styling, making webpages look nice. From the size of the text to the background colors to the positioning of HTML elements, CSS gives you control over almost every visual aspect of a page.


CSS and HTML work in tandem. CSS styles (or rules) are applied directly to HTML elements. For example, remember this element from above - `<h1 id="heading">Darth Vader</h1>`. Well, since there is an `id` selector associated with it, we can assign CSS styles to it using an external stylesheet.

```css
#heading {
  color: pink;
}
```

**Save this as "main.css".**

> There are three ways that you can assign styles to HTML tags. Inline. Internal. Or External. Inline styles are placed directly in the tag; these should be avoided, though, as it's best practice to keep HTML and CSS styles separated (don't mix structure with presentation!). Internal styles fall within the head of a website. Again, these should be avoided as well due to reasons mentioned before. Read more about this [here](http://www.w3schools.com/css/css_howto.asp).

Next, we need to "link" our HTML page and CSS stylesheet. To do so, add the following code to the `<head>` section of the HTML page just below the title:

```html
<link rel="stylesheet" href="main.css">
```

Your code should now look like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="main.css">
    <title>Resume: Darth Vader, Lord of the Sith</title>
  </head>
  <body>
    <h1 id="heading">Darth Vader</h1>
    <p>Lord of the Sith</p>
    <ul>
      <li>Imperial Palace, 000-001</li>
      <li>Hololink: 655321-666</li>
      <li>lordvader@gmail.com</li>
    </ul>
    <br/>
    <img src="http://upload.wikimedia.org/wikipedia/en/7/76/Darth_Vader.jpg">
    <br>
    <h2>History and Profile</h2>
    <p>I am a fearsome cyborg with extensive experience gained as the supreme commander of the Galactic Empire. I successfully delivered the largest strategic initiative within the Star Wars universe, working in partnership with Emperor Palpatine and other key stakeholders to bring the project in on time and within budget, twice because of that cursed rebellion. With a powerful bass voice, imposing body armour and signature respiratory breathing, I am able to use my influence at all levels, whether leading Imperial subordinates, devastating estranged family members, or crushing the Rebel Alliance.</p>
    <h2>Education</h2>
    <ul>
      <li>Jedi Academy, Master warrior-monk and basket weaving</li>
      <li>Obi-Wan Kenobi School of Training, Jedi Training</li>
    </ul>
    <h2>Work History</h2>
    <ul>
      <li>His Excellency Palpatine I, Emperor of the Galaxy - Major General</li>
      <li>The Jedi Order - Liaison to the Supreme Chancellor</li>
      <li>Watto's Junk Dealership - electronics repair</li>
    </ul>
    <h2>Skillset</h2>
    <ul>
      <li>Oppressing the Galaxy</li>
      <li>Great Physical Strength</li>
      <li>Mastery of the Force</li>
      <li>Lightsaber Duels</li>
      <li>Team Leadership</li>
      <li>Imperial Weapons Research</li>
      <li>Ruby Scripting Ninja</li>
      <li>Master pick-pocketter</li>
    </ul>
  </body>
</html>
```

Save the file. Check it out in your browser.

See the difference? 

You can change certain elements even if they are not *explicitly* found within the HTML of the page, like the background color.

Update your CSS file:

```css
body {
  background-color: yellow;
}

#heading {
  color: pink;
}
```

Save. Refresh.

### What's going on?

Look back at the CSS file.

1. We have the `#heading` *selector*, which is associated with the selector in our HTML document, followed by curly braces.
2. Inside the curly braces, we have *properties*, which are descriptive words, like font-weight, font-size, or background color. In our case, we have `color`.
3. *Values* are then assigned to each property, which are preceded by a colon and followed by a semi-colon. [http://cssvalues.com/](http://cssvalues.com/) is an excellent resource for finding the acceptable values given a CSS property. I use this almost everyday.

Can you figure out what's going on with the `body` tag?

### Additional Properties

You can view all the available properties [here](http://www.w3.org/TR/CSS2/propidx.html). Pay attention to the font-related properties - like font-family, font-weight, and font-style - as you will be using these later.

Margins, padding, and borders are also good properties to go over since they appear in almost every web page.

### Putting it all together

1. First, let's add a bootstrap stylesheet via a content delivery network, which is a online repository of commonly used Javascript and CSS files. There are a number of free CDNs available. It's a good practice to use a CDN in your production code, as many of the files are pre-cached, so your site will actually load faster.

  Bootstrap, meanwhile, is a powerful front-end framework. You can create a responsive site that looks good on all devices in no time at all. 

  Add the link to bootstrap to your HTML.

  ```html
  <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/bootswatch/3.1.1/cyborg/bootstrap.min.css">
  ```

  Take a look at your page. That's just from adding one line of code!

2. Add one selector to the HTML:

  ```html
  <p class="lead">Lord of the Sith</p>
  ```

3. Add some dividers:

  ```html
  <div class="container"></div>
  <div class="row"></div>
  <div class="col-md-6">
  ```

  First, we're adding a a `.container`, which literally contains the all the page content. Then we are using the bootstrap [grid](http://getbootstrap.com/css/#grid) system. See the link for more details. 

3. Now, let's update the CSS file.

  ```html
  body {
    background-color: pink;
    font-family: 'Titillium Web', sans-serif;
  }

  h1, h2 {
    font-family: 'Titillium Web', sans-serif;
  }

  #heading {
    font-size: 4em;
    color: pink;
  }

  .lead {
    font-style: italic;
  }

  .container {
    padding: 50px;
    max-width: 800px;
    background-color: black;
  }
  ```

  Make sure to add the font to the `<head>`: 

  ```html
  <link href='http://fonts.googleapis.com/css?family=Titillium+Web' rel='stylesheet' type='text/css'>
  ```

Save. Refresh your browser.

What do you think? Good. Bad. Ugly? Change the color of the background and header on your end. The [color picker](http://color.hailpixel.com/) is nice for finding colors.

## Your turn!

While I provide a brief review, work along with me to develop your own basic site. 

1. Create a basic HTML page with the doctype, html, head, and body tags
2. Add a header (H1)
3. Create an ordered list
4. Add an external CSS file (make sure to link to the HTML page)
4. Change the background color and font size
4. Style the list

Show it off!

## Chrome Developer Tools

Using Chrome Developer Tools, we can not only view how someone added, for example, a CSS selector to make the HTML text to appear to hoover - but it's also an excellent means of testing either HTML or CSS changes directly from the browser. This can save a lot time

Open up the HTML page we worked on. Right Click on the first paragraph. Select "Inspect Element". Notice the styles on the right side of the Developer Tools pane associated with the paragraph. Do you see the styles associated with the first paragraph? Go ahead and change the size of the text.

Change the color of the even rows from black to something super cool.

You can also edit your HTML in real time. With Dev Tools open, right click the text and select "Edit as HTML"

> Be careful as these changes are temporary. Watch what happens when you refresh the page.

## Extra Credit

1. Try some of [these](http://en.wikiversity.org/wiki/Web_Design/HTML_Challenges) challenges.
