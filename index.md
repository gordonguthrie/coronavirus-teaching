# Coronovirus Lets Learn To Code

## Introduction

This is a running curriculum of the class

## Purpose

To have a single point of information

## Scope

Each day I will publish what we are going to learn.

As we get through it we will collect useful website, links and resources and I will update this document with them.

## Things you will need

* the Zoom video conference client installed (https://zoom.us/download#client_4meeting)
* the Firefox web browser installed (https://www.mozilla.org/en-US/firefox/new/)
* the Atom editor installed (https://atom.io/)

## Overall Plan

The plan is to try and get through:

* what is a web page made of?
  * html (HyperText Markup Language - a way of creating structured elements in a webpage)
    * the `<head>` section
    * the `<body>` section
    * basic elements
      * `<div>`
      * `<span>`
      * `<h1>` etc
      * simple form elements
         * no forms posting to a webserver - just input for javascript
  * css (Cascading Style Sheets - a way of making HTML look pretty)
      * basics of CSS
      * selectors/intro to specifity
      * ***advanced*** using a CSS framework (probably Semantic UI)
  * js (Javascript - a programming language)
      * functions
      * scope
        * (and its discontents)
      * the DOM (Domain Object Model - how we make things happen on a webpage in a browser)
        * (and its discontents)
        * ***advanced*** using a JS framework (deffo JQuery)
* building something - an in-page calculator
  * make it look like a calculator
  * collect inputs
  * write a programming language in Javascript to calculate the result
* ***if we have the time***
  * write some music using Sonic Pi (http://sonic-pi.net/)

## Day 1 - Lesson

* getting to know our tools
    * Atom editor
    * Firefox Web Developer Tools
* writing our first web webpage with HTML
    * basic elements
* make our first webpage less ugly with CSS
    * inline styles
* mucking our webpage about with JS
    * from the web console

## Day 1 - Lesson notes

### Day 1a - Small Web Page

Lets build the smallest web page that works. Traditionally in programming this is called `hello world` make your language display the words Hello word.

This is it in `html`

```html
<html>
  <head>
  </head>
  <body>
    hello world
  </body>
</html>
```

This is actually not true - you can make smaller webpages.

### Day 1b - Proper Web Page

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Learning Coding In Lockdown</title>
    <meta name="description" content="My first webpage">
    <meta name="author" content="Gordon">
  </head>
  <body>
    <div>Hello World</div>
  </body>
</html>
```

### Day 1c - Basic Tags

`html` pages are made from tags - which come in two sorts.

* enclosing tags
     * `<div>Hello world</div>`
         * there is an opening tag `<div>`
         * and then a matching closing tag `</div>`
         * these are just like `(` brackets `)` in written English
* self-closing tags
    * `<hr />`

Here are some basic enclosing tags:

* `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
* `<p>`
* `<div>`
* `<span>`

(Remember each opening tag `<div>` needs a closing tag after what it encloses `</div>`)

Here are some basic self-closing tags:

* `<br />`
* `<hr />`

### Day 1d - Nested Tags

Not all tags are stand alone. You need to nest tags inside tags sometimes.

An example is the bullet list and the numbered list

```HTML
<ul>
  <li>hello</li>
  <li>world</li>
</ul>
```

```HTML
<ol>
  <li>hello</li>
  <li>world</li>
</ol>
```

### Day 1e - Exercise 1

Write a short CV, header, paragraph or list, another header, another para or list.

Enclose all you content (words) in tags plz.

### Day 1f - Basic (Inline) Styling with CSS (Cascasding Style Sheet)

There are three ways you can do CSS:

* inline
     * write styles inside tags
* internal
     * write styles in the web page
* external
     * write styles in an external file and include that file into the webpage

  An inline style is just written into the tag:

  * `<p style="color:red;">This is a paragraph.</p>`

Here are some basic styles:

* `style="background-color:DodgerBlue;`
* `style="color:MediumSeaGreen;`
* `style="border: 2px solid Tomato;"`
* `style="border: 2px solid red;"`
* `style="border-radius: 5px;"`
* `style="font-family:"Courier New", Lucida Console, monospace;"`
* `style="font-style:italic;"`

Styles can be combined in a tag:

* `<p style="background-color:gray;color:orange;">This is a paragraph.</p>`

This was the original way of styling elements in html. Its not really scalable, and it technically isn't **Cascading Style Sheets** its just styles.

`CSS` was invented to solve the problem of millions of elements each with dozens of styles - and each bullet point needing to have the same styles applied. Nobody uses `inline` styles (except when they do).

### Day 1g - Mucking about


If we open the `console` in `webtools` in Firefox we can now muck about with stuff.

## Day 1 - Homework

* investigate other webtools
    * Chrome
    * Safari
* investigate other `html` tags and HTML5
    * image
    * links
    * buttons
    * inputs
* investigate other CSS selector operators like
    * `>`
    * `+`
    * `~`
    * `[target]`
    * `[attribute=value]`

## Day 2 - Lesson notes

We will carry on with the CV that we built last lesson.

If you have deleted it just copy this one rather than muck about rewriting it.

```HTML
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Learning Coding In Lockdown</title>
    <meta name="description" content="My first webpage">
    <meta name="author" content="Alice">
  </head>
  <body>
    <h1 style="background-color:gray;color:orange;">Alice Asymptomatika</h1>
    <p>I working in marketing, but am taking the opportunity to learn coding online</p>
    <hr/>
    I would like to learn:
    <ul>
      <li>
        <p>
          HTML <small>(Hypertext Markup Language)</small>
        </p>
      </li>
      <li>
        <p>
          CSS <small>(Cascading Style Sheets)</small>
        </p>
      </li>
      <li>
        <p>
          JS <small>(Javascript)</small>
        </p>
      </li>
    </ul>
    <hr/>
    I would like to learn how to:
    <ol>
      <li>
        <p>
          Design website
        </p>
      </li>
      <li>
        <p>
          Build an app for the phone
        </p>
      </li>
      <li>
        <p>
          Work in tech
        </p>
      </li>
    </ol>

  </body>
</html>
```

### Day 2a - Better (Internal) Styling with CSS (Cascading Style Sheet)

  Here is an internal style. The style rules are the same as in inline styling. The difference is that each style is now preceded with a `selector`.

```HTML
  <style>
  body {
    background-color: linen;
  }
  div {
    color: maroon;
    margin-left: 40px;
  }
  </style>
```

The format is:

* `selector`
* opening curly brackets `{`
* styles which are:
    *  `style type`
    * `:`
    * `style details`
* and closed  by a closing curly bracket `}`

It is enclosed in a style tag and (conventionally) is included in the `<head>` section.

```HTML
  <!doctype html>
  <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Learning Coding In Lockdown</title>
      <meta name="description" content="My first webpage">
      <meta name="author" content="Gordon">
      <style>
      body {
        background-color: linen;
      }
      div {
        color: maroon;
        margin-left: 40px;
      }
      </style>
    </head>
    <body>
      <div>Hello World</div>
      <hr />
      <ul>
        <li>hello</li>
        <li>world</li>
      </ul>
      <ol>
        <li>hello</li>
        <li>world</li>
      </ol>
    </body>
  </html>
```

These styles (with a single selector) apply to all tags of a type - all your paragraphs have the same font size. Lets fix that with some cascading style sheets.

### Day 2b - Cascading Styles

Lets get some text and some bullet points and then style part it.

```HTML
<h1>Gordon Guthrie</h1>
<p>I am a strong technologist with experience of:</p>
<ul>
  <li>
    <p>Erlang</p>
  </li>
  <li>
    <p>Elixir</p>
  </li>
  <li>
    <p>LFE</p>
  </li>
</ul>
```

If we now add the style:

```HTML
<style>
  li p {
    font-style:italic;
  }
</style>
```

This selector `li p` says apply this style to all tags `<p>` inside a pair of `<li>` tags

The style has **cascaded**.

If we edit the style to say:

```HTML
<style>
  h1, li p {
    font-style:italic;
  }
</style>
```

This style now applies to the header as well as the bullet points.

The comma `,` is an operator - its technically a boolean `OR` so the selector `h1, li p` means *if the tag is* `<h1>` *OR the tag is a* `<p>` *inside an* `<li>`.

### Day 2c - Exercise

Add some inline styling to our CV using cascading selectors

### Day 2d - External CSS files

To make it easy to tech and show we are putting our CSS directly into our webpages using the `<style>` tags but this gets cumbersome.

Normally you write your `css` in a different file and then include it into the page.

Our webpage looks a bit ugly and not very distinctive so lets jazz it up with some proper fonts.

At the moment the fonts used to display the webpage are the normal ones that come with the computer but they look a bit shite.

Google hosts a lot of fonts at https://fonts.google.com/ let add them.

We do that by adding this line to the `<head>` of our webpage.

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lobster">
```
This will pull in a special `css` file that makes a webfont available. Webfont `css` is a right monkey business to do yourself so it is best at the moment to just let Google sort it out for us.

We now need to make our webpage use that new font by adding it to the

```html
<style>
      body {
        font-family: 'Lobster', serif;
        font-size: 48px;
      }
    </style>
```

### Day 2e - Exercise

Find two fonts you like that go together on Google.

One for the headline, one for the bodytext.

Use a style sheet to apply them.

### Day 2f - Introduction To REPLs

We are going to start today by writing javascript in the browser console.

The console is an example of a REPL (a Read-Evaluate-Print-Loop).

Lots of `interpreted` languages have REPLs.

Here is a website with online REPLs:

https://repl.it/languages

### Day 2g - Javascript and its discontents

Javascript is a standard language - all web browsers run the same Javascript. That sounds good, but...

Javascript the language interacts with the Browser by call functions that have been exposed on the DOM (Domain Object Model).

A ***Domain*** is a functional area, it might be banking, it might be health checks, it might be anything, but here is ***a browser***.

***Object*** is a term of art - it refers to a programming style where you have a ***thing*** (the object) and it exposes ***functions*** which you call against it. The ***object*** hides its internals from you. Think of it as a control panel with a load of switches and dials. You don't get to see the internal electrics, all you do is toggle the switches and read the dials.

***Model*** is just that a model - we have build an ***object*** set of ***functions*** that model what the browser does and allows you to manipulate all the things we have looked at: `tags` and `styles`.

The problem is that each browser has its own `DOM`. They are **mostly** the same but sometimes the functions have slightly different names, and more often the functions have slightly different behaviours.

Think of it like cash machines. Each cash machine exposes the same functionality (`get cash`, `get balance`), each does it with similar buttons (`numbers`, `help`, `clear`, `submit`) but the buttons are in different places, the amount of money to get out varies. Each `DOM` is like that - it is a cashmachine, just not exactly the same cash machine.

We are going to start by writing a bit of raw `javascript` against the `DOM`. This is the ***first*** and ***last*** time you will ever do this.

If you write `javascript` against the `DOM` then you have to test every time `if this is running in Chrome do this, if it is in Safari do that, if it is in Edge do something else`. This is tremendously tedious.

People ***always*** write `javascript` against libraries and frameworks that **abstract the DOM** and offer a consistent interface.

Later on we will do that with `jquery`. `jquery` is considered a bit old-fashioned now, the cool kids are off on new frameworks like `jsx`, or `angular` or `react` or `ember` or `node`. But the cool kids are always off on something new n `javascript` land.

`javascript` was written in a week to meet a sales deadline. It has a lot of problems - global state. 20 years later a lot of the things you see (frameworks, transpiled languages targetting `javascript`, tool pipelines) are new attempts to fix things laid down in a hurry in that first week.

### Day 2h - Javascript in the console

Lets crack open our web console. Click the `hamburger` menu top left in Firefox to get the options menu and select `Web Developer`:

![Open the menu](./images/firefox_web_console.png)

Then from the second menu select `Web  Console`:

![Open the web console](./images/firefox_select_web_console.png)

This gives us the webpage with the console open at the bottom:

![The web console](./images/browser_with_console_open.png)

We will be using only the basic menu items:

* Inspector
* Console

![Console menu](./images/console_menu.png)

***Lets Code!***

```Javascript
var mydiv = document.querySelector("h1");
```

When you press return this will print `undefined`.

So what is this? What does it mean.

`document` is an object. You remember the ***Domain Object Model*** well that object. And `document` is the name of the webpage you can see in your browser.

`querySelector()` is a function on the object that does something (a switch or a dial). It performs a ***query*** using a selector. That ***selector*** as it happens has the same form as a `css` selector. So here we use `h1` but we could use any of the other `css` selectors we have played with.

We pass that function a set of parameters - in this case the set only has 1 member and it is a ***string*** which describes the selector. The string is `"h1"` and the list of parameters is delimited by `(` and `)`. This enclosing pattern is the same pattern we saw with `html` tags and with `{` and `}` in `css`. It is a fundamental convention of software, languages have a way to mark ***start*** and ***end***, ***alpha*** and ***omega***.

That function returns a value - that value is an ***object***.

The equals operator `=` assigns that value on the right hand side to the left hand side (Arabic numerals, code words right-to-left not left-to-right).

It assigns the `object` to the variable `mydiv`. `mydiv` is a name (`alice`, `bob`, `charlie`) that I, the developer will use to keep track of things. All languages have variables, in most languages they can even vary (not the mighty `Erlang` tho, there variables don't vary, and that's why we luv it).

We know `mydiv` is a variable because we have declared it to be with the `var` ***keyword*** (short for variable).

Each programming language has its set of ***keywords*** that you have to learn. Usually there are about 30 to 50. Keywords are often shared across languages. (See the Day 2 Appendix).

Finally the operator `=` is a function and it doesn't return a result (some javascript functions do something and don't return a value, some do something and return a value).

So the REPL prints the result of the last operation - and that result is `undefined` - no value returned.

The last thing we haven't talked about is `;` which means ***line ending*** in javacript - it is a ***delimiter***. Again delimiters are shared across programming languages.

Lets look at another function.

```Javascript
console.log("bob");
```

Press return and we get `bob`.

Lets break this down again. The ***function*** is called `log` it is taking `"bob"` as a ***parameter*** and the ***function*** is attached to an ***object*** called `console`. The main webpage is an ***object*** called `document` and it turns out the `console` is a webpage ***object*** called `console`.

`log` takes the ***parameter*** it is given and tries to turn it into something readable then print it out in the `console`.

The parameter can be an ***expression*** that evaluates to a single term:

```Javascript
console.log(3+2);
console.log("fish" + "bicycle");
console.log("fish" + 2);
```

Lets use this ***function*** to inspect our variable `mydiv`.

```javascript
console.log(mydiv);
```

We get a big output:

![h1 object](./images/screenshot_of_h1_object.png)

Eek!

If we scroll down we see that there is a thing called `innerText`. This is the text that appears inside the `h1` tag. We can now use `javascript` to rewrite that:

```Javascript
mydiv.innerHTML = "banjo";
```

And it changes on the page.

***Well done, you have done your first bit of  coding!***

### Day 2j - Exercise

Inspect the `h1` object. Select another object (eg `p`) and inspect that too. How similar and how different are they?

Print the `console` object with `console.log` and inspect that. How is it different to a text object like an `h1` or a `p`?

Can you ***clear*** the console?

### Day 2k - Introduction to JFiddle

Lets look at JFiddle - which is the most common way to get help with `html`, `css` and `javascript`.

***I am trying to do X but it doesn't work, here is a link to a JFiddle, can you help me?***.

https://jsfiddle.net/

### Day 2 Homework

Go to https://repl.it/languages and look at the different languages and examples.

Play about with the console and look at the other menus.

Try and find the console in other browsers like Chrome or Safari.

Read the Day 2 Appendix on Javascript Keywords

### Day 2 - Appendix Javascript Keywords

These are the most common javascript keywords:

* boolean
* break
* case
* catch
* char
* const
* do
* double
* else
* false
* float
* for
* function
* if
* in
* instanceof
* int
* new
* null
* return
* true
* try
* typeof
* var
* while

***Don't Panic!*** there is a trick to recognising them. When you write code you typically make up names for things in three styles:

* functions have ***verby*** names `do_something()` like `querySelector()`
* variables have ***nouny*** names: `house`, `car` like `mydiv`
* booleans have ***questiony*** names: `is_condition?` like `is_valid?`, `is_visible?`

Most keywords are ***little words*** (`else`, `while`), ***adjectives*** (`constant`), ***abstract nouns*** (`true`, `false`) or ***blankish verbs*** (`try`, `do`).

Basically if its bland its probably a language keyword, if its vivid its not.

For reference here are the rest:

* abstract
* arguments
* await
* byte
* class
* continue
* debugger
* default
* delete
* enum
* eval
* export
* extends
* final
* finally
* goto
* implements
* import
* interface
* let
* long
* native
* package
* private
* protected
* public
* short
* static
* super
* switch
* synchronized
* this
* throw
* throws
* transient
* void
* volatile
* with
* yield
