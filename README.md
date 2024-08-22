# Intro to CSS

<h3>KEY TAKEAWAY: All HTML elements are boxes made up of four components: a content container, padding, border, and margin. </h3>

Cascading Style Sheets or CSS is a language web developers use to style the HTML content on a web page. If you’re interested in modifying colors, font types, font sizes, images, element positioning, and more, CSS is the tool for the job!

\*In this lesson, you’ll learn how to set up your CSS file structure and select which HTML elements you wish to style.\*

<!-- above \* is me testing the ignore html markdown formatting 
You can tell GitHub to ignore (or escape) Markdown formatting by using \ before the Markdown character.

eg. Let's rename \*our-new-project\* to \*our-old-project\*.
-->

Testing 

````
```
what does this do?
```
````

<body>

<h2>CSS Anatomy</h2>

The diagram on the right shows two different methods, or syntaxes, for writing CSS code. The first syntax shows CSS applied as a ruleset, while the second shows it written as an inline style. Two different methods of writing CSS may seem a bit intimidating at first, but it’s not as bad as it looks!

Both methods contain common features in their anatomy. Notice how both syntaxes contain a declaration. Declarations are the core of CSS. They apply a style to the selected element. Here, the `<p>` element has been selected in both syntaxes and will be styled to display the text in blue.

Understanding that a declaration is used to style a selected element is key to learning how to style HTML documents with CSS! The terms below explain each of the labels in the diagram on the right.

Ruleset Terms:

Selector—The beginning of the ruleset used to target the element that will be styled.
Declaration Block—The code in-between (and including) the curly braces ({ }) that contains the CSS declaration(s).
Declaration—The group name for a property and value pair that applies a style to the selected element.
Property—The first part of the declaration that signifies what visual characteristic of the element is to be modified.
Value—The second part of the declaration that signifies the value of the property.
Inline Style Terms:

Opening Tag—The start of an HTML element. This is the element that will be styled.
Attribute—The style attribute is used to add CSS inline styles to an HTML element.
Declaration—The group name for a property and value pair that applies a style to the selected element.
Property—The first part of the declaration that signifies what visual characteristic of the element is to be modified.
Value—The second part of the declaration that signifies the value of the property.
Don’t worry about memorizing all of these—you will get acquainted with them more and more as the course progresses! Feel free to come back and use this exercise as a reference later on.</p>


<h2>Inline Styles</h2>

<p>
Although CSS is a different language than HTML, it’s possible to write CSS code directly within HTML code using inline styles.

To style an HTML element, you can add the style attribute directly to the opening tag. After you add the attribute, you can set it equal to the CSS style(s) you’d like applied to that element.

```
<p style='color: red;>I'm learning to code!</p>
```

The code in the example above demonstrates how to use inline styling. The paragraph element has a style attribute within its opening tag. Next, the style attribute is set equal to color: red;, which will set the color of the paragraph text to red within the browser.

If you’d like to add more than one style with inline styles, simply keep adding to the style attribute. Make sure to end the styles with a semicolon (;).

```
<p style='color: red; font-size: 20px;'>I'm learning to code!</p>
```

It’s important to know that inline styles are a quick way of directly styling an HTML element, but are rarely used when creating websites. But you may encounter circumstances where inline styling is necessary, so understanding how it works, and recognizing it in HTML code is good knowledge to have. Soon you’ll learn the proper way to add CSS code!
</p>


<h2>Linking the CSS File</h2>

<p>Perfect! We successfully separated structure `(HTML)` from styling `(CSS)`, but the web page still looks bland. Why?

When HTML and CSS codes are in separate files, the files must be linked. Otherwise, the HTML file won’t be able to locate the CSS code, and the styling will not be applied.

You can use the `<link>` element to link HTML and CSS files together. The `<link>` element must be placed within the head of the HTML file. It is a self-closing tag and requires the following attributes:

<ul>
  <li>href — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.</li>
rel — this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to stylesheet.</li>
When linking an HTML file and a CSS file together, the <link> element will look like the following:</li>
</ul>

```
<link href='https://www.codecademy.com/stylesheets/style.css' rel='stylesheet'>
```

Note that in the example above, the path to the stylesheet is a URL:

https://www.codecademy.com/stylesheets/style.css

Specifying the path to the stylesheet using a URL is one way of linking a stylesheet.

If the CSS file is stored in the same directory as your HTML file, then you can specify a relative path instead of a URL, like so:

```
<link href='./style.css' rel='stylesheet'>
```

Using a relative path is very common way of linking a stylesheet.
</p>


<h2>Review</h2>
Great work so far! By understanding how to incorporate CSS code into your HTML file, as well as learning some of the key terms, you’re on your way to creating spectacular websites with HTML and CSS.

Let’s review what you learned so far:
<ul>
<li>The basic anatomy of CSS syntax written for both inline styles and stylesheets.</li>
<li>Some commonly used CSS terms, such as ruleset, selector, and declaration.</li>
<li>CSS inline styles can be written inside the opening HTML tag using the style attribute.</li>
<li>Inline styles can be used to style HTML, but it is not the best practice.</li>
<li>An internal stylesheet is written using the &lt;style&gt; element inside the <head> element of an HTML file.</li>
<li>Internal stylesheets can be used to style HTML but are also not best practice.</li>
<li>An external stylesheet separates CSS code from HTML, by using the .css file extension.</li>
<li>External stylesheets are the best approach when it comes to using HTML and CSS.</li>
<li>External stylesheets are linked to HTML using the &lt;link&gt; element.</li>
<li>Take this knowledge to the next lesson, where you start learning how to select HTML elements to style!</li>
</ul>

Here are a few more resources to add to your toolkit:

Codecademy Docs: CSS <br>
Codecademy Workspaces: CSS








<h1>Type selector</h1>

<p>
Remember that declarations are a fundamental part of CSS because they apply a style to a selected element. But how do you decide which elements will get the style? With a selector.

A selector is used to target the specific HTML element(s) to be styled by the declaration. One selector you may already be familiar with is the type selector. Just like its name suggests, the type selector matches the type of the element in the HTML document.

In the previous lesson, you changed the color of a paragraph element.

```
p {
  color: green;
}
```

This is an instance of using the type selector! The element type is p, which comes from the HTML <p> element.

Some important notes on the type selector:

The type selector does not include the angle brackets.
Since element types are often referred to by their opening tag name, the type selector is sometimes referred to as the tag name or element selector.

<h2>Class</h2>
<p>CSS is not limited to selecting elements by their type. As you know, HTML elements can also have attributes. When working with HTML and CSS a class attribute is one of the most common ways to select an element.

For example, consider the following HTML:

```
<p class='brand'>Sole Shoe Company</p>
```

The paragraph element in the example above has a class attribute within the opening tag of the<p> element. The class attribute is set to 'brand'. To select this element using CSS, we can create a ruleset with a class selector of .brand.

```
.brand {

}
```

To select an HTML element by its class using CSS, a period (.) must be prepended to the class’s name. In the example above, the class is brand, so the CSS selector for it is .brand.
</p>






<h2>Universal</h2>

You learned how the type selector selects all elements of a given type. Well, the universal selector selects all elements of any type.

Targeting all of the elements on the page has a few specific use cases, such as resetting default browser styling, or selecting all children of a parent element. Don’t worry if you don’t understand the use cases right now—we will get to them later on in our Learn CSS journey.

The universal selector uses the * character in the same place where you specified the type selector in a ruleset, like so:

```
* { 
  font-family: Verdana;
}
```

In the code above, every text element on the page will have its font changed to Verdana.







<h2>Multiple Classes</h2>

We can use CSS to select an HTML element’s class attribute by name. And so far, we’ve selected elements using only one class name per element. If every HTML element had a single class, all the style information for each element would require a new class.

Luckily, it’s possible to add more than one class name to an HTML element’s class attribute.

For instance, perhaps there’s a heading element that needs to be green and bold. You could write two CSS rulesets like so:

```
.green {
  color: green;
}

.bold {
  font-weight: bold;
}
```

Then, you could include both of these classes on one HTML element like this:

```
<h1 class='green bold'> ... </h1>
```

We can add multiple classes to an HTML element’s class attribute by separating them with a space. This enables us to mix and match CSS classes to create many unique styles without writing a custom class for every style combination needed.




<h2>ID</h2>

Oftentimes it’s important to select a single element with CSS to give it its own unique style. If an HTML element needs to be styled uniquely, we can give it an ID using the id attribute.

```
<h1 id='large-title'> ... </h1>
```

In contrast to class which accepts multiple values, and can be used broadly throughout an HTML document, an element’s id can only have a single value, and only be used once per page.

To select an element’s ID with CSS, we prepend the id name with a number sign (#). For instance, if we wanted to select the HTML element in the example above, it would look like this:

```
#large-title {

}
```

The id name is large-title, therefore the CSS selector for it is #large-title.


<h2>Attribute</h2>

You may remember that some HTML elements use attributes to add extra detail or functionality to the element. Some familiar attributes may be href and src, but there are many more—including class and id!

The attribute selector can be used to target HTML elements that already contain attributes. Elements of the same type can be targeted differently by their attribute or attribute value. This alleviates the need to add new code, like the class or id attributes.

Attributes can be selected similarly to types, classes, and IDs.

```
[href]{
   color: magenta;
}
```

The most basic syntax is an attribute surrounded by square brackets. In the above example: [href] would target all elements with an href attribute and set the color to magenta.

And it can get more granular from there by adding type and/or attribute values. One way is by using type[attribute*=value]. In short, this code selects an element where the attribute contains any instance of the specified value. Let’s take a look at an example.

```
<img src='/images/seasons/cold/winter.jpg'>
<img src='/images/seasons/warm/summer.jpg'>
```

The HTML code above renders two &lt;img&lt; elements, each containing a src attribute with a value equaling a link to an image file.

```
img[src*='winter'] {
  height: 50px;
}

img[src*='summer'] {
  height: 100px; 
}
```

Now take a look at the above CSS code. The attribute selector is used to target each image individually.

The first ruleset looks for an img element with an attribute of src that contains the string 'winter', and sets the height to 50px.
The second ruleset looks for an img element with an attribute of src that contains the string 'summer', and sets the height to 100px.
Notice how no new HTML markup (like a class or id) needed to be added, and we were still able to modify the styles of each image independently. This is one advantage to using the attribute selector!
</p>



<h2>Pseudo-class</h2>

You may have observed how the appearance of certain elements can change, or be in a different state, after certain user interactions. For instance:

<ul>
  <li>When you click on an <input> element, and a blue border is added showing that it is in focus.</li>
  <li>When you click on a blue <a> link to visit to another page, but when you return the link’s text is purple.</li>
  <li>When you’re filling out a form and the submit button is grayed out and disabled. But when all of the fields have been filled out, the button has color showing that it’s active.</li>
</ul>

These are all examples of pseudo-class selectors in action! In fact, :focus, :visited, :disabled, and :active are all pseudo-classes. Factors such as user interaction, site navigation, and position in the document tree can all give elements a different state with pseudo-class.

A pseudo-class can be attached to any selector. It is always written as a colon : followed by a name. For example p:hover.

```
p:hover {
  background-color: lime;
}
```

In the above code, whenever the mouse hovers over a paragraph element, that paragraph will have a lime-colored background.



<h2>Classes and IDss</h2>
<p>
CSS can select HTML elements by their type, class, and ID. CSS classes and IDs have different purposes, which can affect which one you use to style HTML elements.

CSS classes are meant to be reused over many elements. By writing CSS classes, you can style elements in a variety of ways by mixing classes. For instance, imagine a page with two headlines. One headline needs to be bold and blue, and the other needs to be bold and green. Instead of writing separate CSS rules for each headline that repeat each other’s code, it’s better to write a .bold CSS rule, a .green CSS rule, and a .blue CSS rule. Then you can give one headline the bold green classes, and the other the bold blue classes.

While classes are meant to be used many times, an ID is meant to style only one element. As you’ll learn in the next exercise, IDs override the styles of types and classes. Since IDs override these styles, they should be used sparingly and only on elements that need to always appear the same.
</p>





<h2>Specificity</h2>

Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity so that if an element needs a new style, it is easy to override.

IDs are the most specific selector in CSS, followed by classes, and finally, type. For example, consider the following HTML and CSS:

```
<h1 class='headline'>Breaking News</h1>

h1 {
  color: red;
}

.headline {
  color: firebrick;
}
```

In the example code above, the color of the heading would be set to firebrick, as the class selector is more specific than the type selector. If an ID attribute (and selector) were added to the code above, the styles within the ID selector’s body would override all other styles for the heading.

Over time, as files grow with code, many elements may have IDs, which can make CSS difficult to edit since a new, more specific style must be created to change the style of an element.

To make styles easy to edit, it’s best to style with a type selector, if possible. If not, add a class selector. If that is not specific enough, then consider using an ID selector.




```
Below is to test/show how the overwrite works, the most specific target selector overwrites the others

Target line =  <h5 class='author-class' id='author-id'>By: Stacy Gray</h5>


h5 {
  color: yellow;
}

.author-class {
  color: pink;
}

#author-id {
  color: cornflowerblue;
}



Each of these rules selects the same element in a different way. Which style will win the “specificity war”? Click “Run” to find out!

Because ID is the most specific selector, the element will change to *cornflower blue*. You may have noticed the other <h5> elements changed to yellow. This is because the most specific (and only) selector they have is their type.
```




<p>Mid-review</p>

```
1.) ID selector - Style ID
#name of id {}

style class/group of certain elements
.name of the class group {}

2.) Element selector - style all element of this type
p{}


3.) Universal selector, style everything in page
*{}

4.) pseudo class :hover, make style appear when mouse hover over. this is one of many unique kinds (:focus, :visited, :disabled, and :active)
p:hover{}


5.) Attribute selector - style any that has the target attribute
img[src*='a string variable/word that is inside the source link'] {
  height: 50px;
}

you can combine element selector and attribute selector to style specific element + attribute combos.

a[href*='florence'] {
  color: lightgreen;
}

Similarly, you can combo together different class selectors

.green {
  color: green;
}

.bold {
  font-weight: bold;
}

so you put class='green bold' in target tag/element and that tag/element will get both green and bold style

```


<p>Chaining</p>

You can combo different selectors, like element + class selector, element + attribute

```
h1.special {
}

The code above would select only the <h1> elements with a class of special. If a <p> element also had a class of special, the rule in the example would not style the paragraph.
```




<h2>Descendant Combos</h2>

In addition to chaining selectors to select elements, CSS also supports selecting elements that are nested within other HTML elements, also known as descendants. For instance, consider the following HTML:

```
<ul class='main-list'>
  <li> ... </li>
  <li> ... </li>
  <li> ... </li>
</ul>
```

The nested &lt;li&gt; elements are descendants of the &lt;ul&gt; element and can be selected with the descendant combinator like so:

```
.main-list li {

}
```







In the example above, .main-list selects the element with the.main-list class (the &lt;ul&gt; element). The descendant &ltli&gt‘s are selected by adding li to the selector, separated by a space. This results in .main-list li as the final selector.

Selecting elements in this way can make our selectors even more specific by making sure they appear in the context we expect.

</body>




<h2>Chaining and Specificity</h2>

In the last exercise, instead of selecting all <h5> elements, you selected only the <h5> elements nested inside the .description elements. This CSS selector was more specific than writing only h5. Adding more than one tag, class, or ID to a CSS selector increases the specificity of the CSS selector.

For instance, consider the following CSS:

```
p {
  color: blue;
}

.main p {
  color: red;
}
```

Both of these CSS rules define what a <p> element should look like. Since .main p has a class and a p type as its selector, only the <p> elements inside the .main element will appear red. This occurs despite there being another more general rule that states <p> elements should be blue.

Exercise answer is:


```

This the index.html part that is changed
 <h2 class='heading-background'> More Destinations </h2>
  <ul>
    <li><h4 class='destination'>Jackson Hole, Wyoming</h4></li>
    <li><h4 class='destination'>Cape Town, South Africa</h4></li>
    <li><h4 class='destination'>La Paz, Bolivia</h4></li>
  </ul>



li h4 {
  color: gold;
}

h4 is descendant/child of li tag, not the ul tag. You can actually put like this, it's basically parent-selector, then descendant-sector, in that order

parent-selector descendant-selector {
  declaration
}

later below was added to show that the more specified selector overwrites this more general selector here
h4 {
  color: dodgerblue;
} 

```




<h2>Multiple Selectors</h2>

In order to make CSS more concise, it’s possible to add CSS styles to multiple CSS selectors all at once. This prevents writing repetitive code.

For instance, the following code has repetitive style attributes:

```
h1 {
  font-family: Georgia;
}

.menu {
  font-family: Georgia;
}
```

Instead of writing font-family: Georgia twice for two selectors, we can separate the selectors by a comma to apply the same style to both, like this:

```
h1, 
.menu {
  font-family: Georgia;
}
```

By separating the CSS selectors with a comma, both the &lt;h1&gt; elements and the elements with the menu class will receive the font-family: Georgia styling.


You can chain element tags too like below, exercise answer.

```
h5, li {font-family: monospace;}
```

<h2>Review</h2>

Throughout this lesson, you learned how to select HTML elements with CSS and apply styles to them. Let’s review what you learned:

<ul>
<li>CSS can select HTML elements by type, class, ID, and attribute.</li>
<li>All elements can be selected using the universal selector.</li>
<li>An element can have different states using the pseudo-class selector.</li>
<li>Multiple CSS classes can be applied to one HTML element.</li>
<li>Classes can be reusable, while IDs can only be used once.</li>
<li>IDs are more specific than classes, and classes are more specific than type. That means IDs will override any styles from a class, and classes will override any styles from a type selector.</li>
<li>Multiple selectors can be chained together to select an element. This raises the specificity but can be necessary.</li>
<li>Nested elements can be selected by separating selectors with a space.</li>
<li>Multiple unrelated selectors can receive the same styles by separating the selector names with commas.</li>
<li>Great work this lesson. With this knowledge, you’ll be able to use CSS to change the look and feel of websites to make them look great!</li>
</ul>





<h2>Introduction To Visual Rules</h2>

The purpose of CSS is to add style to web page, and each element on the page can have many style properties. Some of the basic properties relate to the size, style, and color of the element. In this lesson, you’ll learn some fundamental CSS visual rules that you can use to start styling web page elements!


<h3>Important Links</h3>
https://discuss.codecademy.com/t/guide-how-to-build-a-web-dev-portfolio/394816?_gl=1*1ly3w0e*_ga*ODk0NDg4NDY4Ni4xNzExNzExNjU5*_ga_3LRZM6TM9L*MTcxMzE2NzE3Ny4zMC4xLjE3MTMxNjk2NjUuMjEuMC4w


What the hell is font-face? How users can see the unique fonts on your website even though they never install that font? IT GETS IT FROM the Font-face file from THE WEBSITE'S SERVER


<h2>Font Family</h2>

<h2>Font Size</h2>



<h2>Font Weight</h2>
In CSS, the font-weight property controls how bold or thin text appears.

```
p {
  font-weight: bold;
}
```

In the example above, all paragraphs on the web page would appear bolded.

The font-weight property has another value: normal. Why does it exist?

If we wanted all text on a web page to appear bolded, we could select all text elements and change their font weight to bold. If a certain section of text was required to appear normal, however, we could set the font weight of that particular element to normal, essentially shutting off bold for that element.



<br>

<h2>Review Visual Rules</h2>

Incredible work! You used CSS to alter text and images on a website. Throughout this lesson, you learned concepts including:

<ul>
  <li>The font-family property defines the typeface of an element.</li>
  <li>font-size controls the size of text displayed.</li>
  <li>font-weight defines how thin or thick text is displayed.</li>
  <li>The text-align property places text in the left, right, or center of its parent container.</li>
  <li>Text can have two different color attributes: color and background-color. color defines the color of the text, while background-color defines the color behind the text.</li>
  <li>CSS can make an element transparent with the opacity property.</li>
  <li>CSS can also set the background of an element to an image with the background-image property.</li>
  <li>The !important flag will override any style, however it should almost never be used, as it is extremely difficult to override.</li>
</ul>



[![Learn CSS Visual Rules](https://www.youtube.com/watch?v=InA5Ff7mxrc&t=3s/0.jpg)](https://www.youtube.com/watch?v=InA5Ff7mxrc&t=3s)


<h2>Box Model</h2>

Review

In this lesson, we covered the four properties of the box model: height and width, padding, borders, and margins. Understanding the box model is an important step towards learning more advanced HTML and CSS topics. Let’s take a minute to review what you learned:

<ul>
  <li>The box model comprises a set of properties used to create space around and between HTML elements.</li>
  <li>The height and width of a content area can be set in pixels or percentages.</li>
  <li>Borders surround the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.</li>
  <li>Padding is the space between the content area and the border. It can be set in pixels or percent.</li>
  <li>Margin is the amount of spacing outside of an element’s border.</li>
  <li>Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.</li>
  <li>Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.</li>
  <li>margin: 0 auto horizontally centers an element inside of its parent content area, if it has a width.</li>
  <li>The overflow property can be set to display, hidden, or scroll, and dictates how HTML will render content that overflows its parent’s content area.</li>
  <li>The visibility property can hide or show elements.</li>
</ul>









<h2>Changing the Box Model</h2>

Why Change the Box Model?

The last lesson focused on the most important aspects of the box model: box dimensions, borders, padding, and margin.

The box model, however, has an awkward limitation regarding box dimensions. This limitation is best illustrated with an example.

```
<h1>Hello World</h1>

h1 {
  border: 1px solid black;
  height: 200px;
  width: 300px;
  padding: 10px;
}
```

In the example above, a heading element’s box has solid, black, 1 pixel thick borders. The height of the box is 200 pixels, while the width of the box is 300 pixels. A padding of 10 pixels has also been set on all four sides of the box’s content.

Unfortunately, under the current box model, the border thickness and the padding will affect the dimensions of the box.

The 10 pixels of padding increases the height of the box to 220 pixels and the width to 320 pixels. Next, the 1-pixel thick border increases the height to 222 pixels and the width to 322 pixels.

Under this box model, the border thickness and padding are added to the overall dimensions of the box. This makes it difficult to accurately size a box. Over time, this can also make all of a web page’s content difficult to position and manage.

In this brief lesson, you’ll learn how to use a different technique that avoids this problem altogether.

<h3>Review: Changing the Box Model</h3>

In this lesson, you learned about an important limitation of the default box model: box dimensions are affected by border thickness and padding.

Let’s review what you learned:

<ul>
  <li>In the default box model, box dimensions are affected by border thickness and padding.</li>
  <li>The box-sizing property controls the box model used by the browser.</li>
  <li>The default value of the box-sizing property is content-box.</li>
  <li>The value for the new box model is border-box.</li>
  <li>The border-box model is not affected by border thickness or padding.</li>
</ul>
<br>
https://css-tricks.com/snippets/css/using-font-face-in-css/







<h2>Display And Positioning</h2>
<h3>Flow of HTML</h3>

A browser will render the elements of an HTML document that has no CSS from left to right, top to bottom, in the same order as they exist in the document. This is called the flow of elements in HTML.

In addition to the properties that it provides to style HTML elements, CSS includes properties that change how a browser positions elements. These properties specify where an element is located on a page, if the element can share lines with other elements, and other related attributes.

In this lesson, you will learn five properties for adjusting the position of HTML elements in the browser:

<li>position</li>
<li>display</li>
<li>z-index</li>
<li>float</li>
<li>clear</li>

Each of these properties will allow us to position and view elements on a web page. They can be used in conjunction with any other styling properties you may know.


<h3>Review</h3>

Great job! In this lesson, you learned how to control the positioning of elements on a web page.

Let’s review what you’ve learned so far:

<ul>
  <li>The position property allows you to specify the position of an element.</li>
  <li>When set to relative, an element’s position is relative to its default position on the page.</li>
  <li>When set to absolute, an element’s position is relative to its closest positioned parent element. It can be pinned to any part of the web page, but the element will still move with the rest of the document when the 
      page is scrolled.</li>
  <li>When set to fixed, an element’s position can be pinned to any part of the web page. The element will remain in view no matter what.</li>
  <li>When set to sticky, an element can stick to a defined offset position when the user scrolls its parent container.</li>
  <li>The z-index of an element specifies how far back or how far forward an element appears on the page when it overlaps other elements.</li>
  <li>The display property allows you to control how an element flows vertically and horizontally in a document.</li>
  <li>inline elements take up as little space as possible, and they cannot have manually adjusted width or height.</li>
  <li>block elements take up the width of their container and can have manually adjusted heights.</li>
  <li>inline-block elements can have set width and height, but they can also appear next to each other and do not take up their entire container width.</li>
  <li>The float property can move elements as far left or as far right as possible on a web page.</li>
  <li>You can clear an element’s left or right side (or both) using the clear property.</li>
  <li>When combined with an understanding of the box model, positioning can create visually appealing web pages. So far, we’ve focused on adding content in the form of text to a web page. In the next unit, you’ll learn 
      how to add and manipulate images to a web page.</li>
</ul>





<h2>Colors</h2>
See Codeacademy lessons, better picture





<h2>Typography</h2>

In this lesson, we’ll focus on typography, the art of arranging text on a page. We’ll look at:

How to style and transform fonts.
How to lay text out on a page.
and how to add external fonts to your web pages.
Some of the most important information a user will see on a web page will be textual. Styling text to make page content accessible and engaging can significantly improve user experience. Let’s begin!



<h4>Web fonts using @font-face</h4>

When you have the files you need, move them to a folder inside your website’s working directory, and you’re ready to use them in a @font-face ruleset!

```
@font-face {
  font-family: 'MyParagraphFont';
  src: url('fonts/Roboto.woff2') format('woff2'),
       url('fonts/Roboto.woff') format('woff'),
       url('fonts/Roboto.ttf') format('truetype');
}
```

Let’s take a look at the example above, line by line:

The @font-face at-rule is used as the selector. It’s recommended to define the @font-face ruleset at the top of your CSS stylesheet.

Inside the declaration block, the font-family property is used to set a custom name for the downloaded font. The name can be anything you choose, but it must be surrounded by quotation marks. In the example, the font is named 'MyParagraphFont', as this font will be used for all paragraphs.

The src property contains three values, each specifying the relative path to the font file and its format. In this example, the font files are stored inside a folder named fonts within the working directory.
Note that the ordering for the different formats is important because our browser will start from the top of the list and search until it finds a font format that it supports. Read more on format prioritization on CSS-Tricks (https://css-tricks.com/snippets/css/using-font-face-in-css/).

Once the @font-face at-rule is defined, you can use the font in your stylesheet!




<h3>Review</h3>

Great job! You learned how to style an important aspect of the user experience—typography.

Let’s review what you’ve learned so far:

<ul>
  <li>Typography is the art of arranging text on a page.</li>
  <li>Text can appear bold or thin with the font-weight property.</li>
  <li>Text can appear in italics with the font-style property.</li>
  <li>The vertical spacing between lines of text can be modified with the line-height property.</li>
  <li>Serif fonts have extra details on the ends of each letter. Sans-Serif fonts do not.</li>
  <li>Fallback fonts are used when a certain font is not installed on a user’s computer.</li>
  <li>The word-spacing property changes how far apart individual words are.</li>
  <li>The letter-spacing property changes how far apart individual letters are.</li>
  <li>The text-align property changes the horizontal alignment of text.</li>
  <li>Google Fonts provides free fonts that can be used in an HTML file with the <link> tag or the @font-face property.</li>
  <li>Local fonts can be added to a document with the @font-face property and the path to the font’s source.</li>
  <li>Using your new knowledge of CSS typography, feel free to edit the code further to make the web page more appealing!</li>
</ul>


</body>

