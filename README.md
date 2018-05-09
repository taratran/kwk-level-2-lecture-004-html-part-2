# Introduction to HTML Part 2

## Objectives

In this lecture, we will take a deeper dive into HTML fundamentals, taking a look at some important elements and at how to layout HTML on a web page.

## SWBATS

HTML - Use specific HTML elements, such as links
HTML - Create visual HTML elements
HTML - Understand basic page structure

## INTRODUCTION

*Note:* Start from scratch on a new HTML file, set up the document structure
once again and put a basic element, such as a 'div' on the page as a review.

So far, we've built valid HTML pages and learned how to get elements and text to
show up on the screen. We've seen `div`, `h1`, and `img`.  These are  great;
with just a few elements like these we can actually do quite a lot in building
out content on a website.  Take a look at https://www.kodewithklossy.com/. With
some _styling_, of course, the look of the website page could actually be
created almost entirely with just `div`, `h1`, and `img` elements.  The top
black navigation bar is one div, and inside it contains an image of the Kode
with Klossy logo.. each box of content below the navigation, including the
video, the Mission and Program sections, the footer...  

However, there is one critical part we still need that we haven't talked about
yet: _Links_

#### HTML Links

On the Kode with Klossy website, when you click on the text in the top navigation,
or on the social media icons, you're clicking a link to either another part
of the Klossy website, or to an entirely different site. Links are the basic
building block that makes up the interconnectivity of the internet, and makes it
possible to navigate around your favorite sites.

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
<a href="https://www.w3schools.com/html/html_links.asp"><img src="cute_doggo.jpg"></a>
```

With the HTML above the image, `cute-doggo.jpg`, would be _clickable_, and would take a site visitor to the html links w3 reference page.

#### Page Structure and Layout

In the last section, we saw how HTML elements can be stuck inside each other.
We often refer to inner HTML elements as the _child_ elements of the _parent_
element, the one that wraps everything, and this ability to nest elements within
each other gives us a huge amount of flexibility when setting up the structure
of a web page.


```html
<body>
  <div>
    <h1>My Totally Awesome Website</h1>
    <h2>No really, it's awesome!</h2>
  </div>
  <div>
    <p>Here in this example, my header content is separated into a different 'div'</p>
    <img src="cool_image.jpg">
    <p>My main text content is inside 'p' tags in their own 'div'</p>
  </div>
</body>
```

In the example above, we could have written it _without the divs_, so why put
them in? For a few reasons really.  For one, we do this for organization: HTML
content can get messy pretty quick, so keeping things sectioned off into
distinct areas of content is helpful for readability.

The other main reason is styling. When we get to CSS, we will be able to apply
custom styling to specific elements in our HTML, or in _sections_ of our HTML.
So, in this example, we may eventually want to style all our header tags to be a
special font.. we can actually apply that style to the div that wraps our
headers.

When making a website or web application, designers will set up separate HTML element sections for navigation, headers, footers, main content, etc.. so much so that in there are a number of
HTML elements with these names:

```html
<nav></nav>
<header></header>
<main>
  <section></section>
  <section></section>
</main>
<footer></footer>
```

All of these elements are basic `div` tags, but given an alias to help use think
about structure.

**Student 10 minute Student Empowerment Pair Exercise:** Students
should the break up into small groups and work on the following:

  - Create a new HTML file and, using the HTML elements just discussed:
    - Create a navigation with a few links to some of their favorite websites
    - Create a header area with a page title and sub title inside
    - Create a main area with any sort of HTML content - sections, images, links
    - Stretch: Use in-line styling that was discussed in the previous lecture to
    make some of these sections different colors

## Moving Forward

When you go to your favorite websites, look closely at how they are laid out. In
fact, try looking at some of them in the Chrome inspector.

Each box of content on a web page, all the images, the links, each section...
behind it all is HTML and _you_ know how to read it now.  Again, don't get
worried if you haven't memorized everything or fully understand how each
element works.  HTML is often trial and error and looking up what the right
syntax is for.  With patience and practice, we can design and build any sort of
web page.

Next up, we will be discussing how to take the HTML we've learned and give it
some _style_.
