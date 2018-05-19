# Introduction to HTML Part 2

## Objectives

In this lecture, we will take a deeper dive into HTML fundamentals. We will
begin by exploring some of the more important elements and follow up with
exploring how HTML can be used to effectively lay out a page. 

## SWBATS

+ HTML - Use specific HTML elements (particularly links)
+ HTML - Create visual HTML elements
+ HTML - Understand basic page structure

## INTRODUCTION

**Note:** This lecture is meant to be coded/progressed in front of the students.
It should be a back and forth between lecture/introducing a concept, and then
showing it in real time on the big screen. Start from scratch on a new HTML
file, set up the document structure once again, and put a basic element, such
as a `<div>`, on the page as a review before beginning.

So far, we've built HTML pages and learned how to get elements and text to
render in the browser. We've seen `<div>`, `<h1>`, and `<img>`. These are great;
with just a few elements like these we can actually do quite a lot in building
out content on a website. 

Let's Take a look at https://www.kodewithklossy.com/ as an example. With some
minor _styling_ (CSS) here and there, the landing page could be created almost
entirely with just `<div>`, `<h1>`, and `<img>` elements. The top black
navigation bar is one `<div>`, and it contains an image of the Kode With Klossy
logo. 

**NOTE:** Show this in Chrome (an extremely useful tool is the element selector,
which can be accessed either by clicking the top left icon in the developer
tools window, or by pressing `cmd + shift + c`). Ask students to call out what
they think individual elements may be while scrolling through the page. 

Try eyeballing each box of content below the navigation, including the video,
the Mission and Program sections, the footer...

With just a little bit of training we can start picking apart a website and
identifying DOM elements. We have to apologize: from here on out you will start
seeing pages as a developer, instead of your average user. Indeed, it is a
blessing and a curse!

However, there is one critical part we still need that we haven't talked about
yet: _Links_

### HTML Links

Let's return to the Kode with Klossy website: when you click on the text in the
top navigation, or on the social media icons, you're clicking a link to either
another part of the Klossy website, or to an entirely different site. Links are
the basic building block that makes up the interconnectivity of the internet,
and makes it possible to navigate around your favorite sites.

We create links using the _anchor link_ element, written as `<a>`:

```html
<a href='a_url_path'>
```

The `<a>` tag requires in an `href` attribute to tell the browser where we want
the link to go to. Links can go inside other elements, like so:

```html
<div>
  <p>
    Here is an example of <a href="https://en.wikipedia.org/wiki/Hyperlink">a link going to Wikipedia</a>
  </p>
</div>
```

..and they can also _wrap_ elements:

```html
<a href="https://www.w3schools.com/html/html_links.asp"><img src="https://i.imgflip.com/1c2b4y.jpg"></a>
```

**NOTE:** Ask the students what they expect the above would do after you write it out in your lecture .html file. (The image itself becomes the link, and we can click it).

Because the anchor tag `<a>` wraps our image, it would be _clickable_, and would
take a site visitor to the referenced W3School's page.

#### Page Structure and Layout

 In the last section, we saw how HTML elements can be wrapped inside one
another. We often refer to an inner HTML element as the _child_, and it's outer
wrapping element the _parent_.  This ability to nest elements within each other
gives us a huge amount of flexibility when setting up the structure of a web
page:

```html
<body>
  <div>
    <h1>My Totally Awesome Website</h1>
    <h2>No really, it's awesome!</h2>
  </div>
  <br />
  <div>
    <p>Here in this example, my header content is separated into a different 'div' above</p>
    <img src="https://i.imgur.com/9y57U8l.jpg">
    <p>My main text content (all this stuff ^!) is inside 'p' tags in their own 'div'</p>
  </div>
</body>
```
#### CFU: Big Group Question
Ask the students, "Why do you think we divided the page in that way?" 
Answers should lead to two big concepts behind <div>: 1. to be able to read code easily and quickly 2. for later on in order to style sectioned out HTMl


In the example above, we could have written it _without the divs_, so why put
them in? For a few reasons really. For one, we do this for organization: HTML
content can get messy pretty quickly, so keeping things sectioned off into
distinct areas of content is helpful for readability.

The other main reason is to make styling easy. When we get to CSS, we will be
able to apply custom styling to specific elements in our HTML, or to _sections_
of our HTML.

So, in this example, we are keeping our HTML organized because we:
  - Want to be able to read the code easily and quickly (which helps us update/edit)
  - May eventually want to add styling that benefits from sectioned out HTML (i.e., we could make sure all our header tags within only the top area of the page have a special font by applying the font to their _parent_)

When making a website or web application, designers will set up separate HTML
element sections for navigation, headers, footers, main content, etc... In fact,
those are such common sections to want on a web page that there exist tags for
them: 

```html
<nav></nav>
<header></header>
<main>
  <section></section>
  <section></section>
</main>
<footer></footer>
```

All of these elements are basic `<div>` tags, but given an alias to help use reason about, style, and organize our structure.

**Student 10 Minute Empowerment Pair Exercise:** Students should break up into small groups and work on the following, checking their results in the browser:

  - Create a new HTML file and, using the HTML elements just discussed:
    - Create a navigation with a few links to some of their favorite websites
    - Create a header area with a page title and sub title inside
    - Create a main area with any sort of HTML content - sections, images, links
    - Stretch: Use in-line styling (Google-fu!) to color different sections and beyond

## Moving Forward

When you go to your favorite websites, look closely at how they are laid out.
See if you can accurately guess which elements are used for which parts of the
rendered page. Don't forget to use Chrome Inspector to see how close you are!

Each box of content on a web page, all the images, the links, every section...
behind it all is HTML and _you_ know how to read it now. Again, don't get
worried if you haven't memorized everything or fully understand when to use what
element. While learning, HTML is often trial, error, and constant referencing of
online documentation. With patience and practice, we can design and build any
sort of web page!

Next up, we will be discussing how to take the HTML we've learned and give it
some _style_.
