# Intro to CSS

Cascading Style Sheets or CSS is a language web developers use to style the HTML content on a web page. If you’re interested in modifying colors, font types, font sizes, images, element positioning, and more, CSS is the tool for the job!

In this lesson, you’ll learn how to set up your CSS file structure and select which HTML elements you wish to style.

<body>

<h2>CSS Anatomy</h2>

<p>The diagram on the right shows two different methods, or syntaxes, for writing CSS code. The first syntax shows CSS applied as a ruleset, while the second shows it written as an inline style. Two different methods of writing CSS may seem a bit intimidating at first, but it’s not as bad as it looks!

Both methods contain common features in their anatomy. Notice how both syntaxes contain a declaration. Declarations are the core of CSS. They apply a style to the selected element. Here, the <p> element has been selected in both syntaxes and will be styled to display the text in blue.

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

&lt;p style='color: red;'&gt;I'm learning to code!&lt;/p&gt;

The code in the example above demonstrates how to use inline styling. The paragraph element has a style attribute within its opening tag. Next, the style attribute is set equal to color: red;, which will set the color of the paragraph text to red within the browser.

If you’d like to add more than one style with inline styles, simply keep adding to the style attribute. Make sure to end the styles with a semicolon (;).

&lt;p style='color: red; font-size: 20px;'&gt;I'm learning to code!&lt;/p&gt;

It’s important to know that inline styles are a quick way of directly styling an HTML element, but are rarely used when creating websites. But you may encounter circumstances where inline styling is necessary, so understanding how it works, and recognizing it in HTML code is good knowledge to have. Soon you’ll learn the proper way to add CSS code!
</p>


<h2>Linking the CSS File</h2>

<p>Perfect! We successfully separated structure (HTML) from styling (CSS), but the web page still looks bland. Why?

When HTML and CSS codes are in separate files, the files must be linked. Otherwise, the HTML file won’t be able to locate the CSS code, and the styling will not be applied.

You can use the <link> element to link HTML and CSS files together. The <link> element must be placed within the head of the HTML file. It is a self-closing tag and requires the following attributes:

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





</body>





