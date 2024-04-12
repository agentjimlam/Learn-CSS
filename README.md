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

```

Perfect! We successfully separated structure (HTML) from styling (CSS), but the web page still looks bland. Why?

When HTML and CSS codes are in separate files, the files must be linked. Otherwise, the HTML file won’t be able to locate the CSS code, and the styling will not be applied.

You can use the <link> element to link HTML and CSS files together. The <link> element must be placed within the head of the HTML file. It is a self-closing tag and requires the following attributes:

href — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.
rel — this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to stylesheet.
When linking an HTML file and a CSS file together, the <link> element will look like the following:

<link href='https://www.codecademy.com/stylesheets/style.css' rel='stylesheet'>

Note that in the example above, the path to the stylesheet is a URL:

https://www.codecademy.com/stylesheets/style.css

Specifying the path to the stylesheet using a URL is one way of linking a stylesheet.

If the CSS file is stored in the same directory as your HTML file, then you can specify a relative path instead of a URL, like so:

<link href='./style.css' rel='stylesheet'>

Using a relative path is very common way of linking a stylesheet.

```



</body>


