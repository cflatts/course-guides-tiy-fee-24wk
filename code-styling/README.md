Handy Code Styling Guide
-------------------------------------------------------


HTML Documents
-------------------------

The basic structure of an HTML file is:

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8" />
        <meta content="ie=edge" http-equiv="x-ua-compatible" />
        <title></title>
    </head>
    <body>

    <script src='[ROUTE TO JS]'></script>
    </body>
    </html>

> **Note:**

> - Both `meta` tags must be included in all files
> - The JS scripts are located at the bottom of the `body` (right before the closing body tag `</body>`)
> - The `script` element has an opening `<script>` and closing `</script>`, regardless of embedding the code here, or linking to an outside file


----------

**HTML Tags**

Every opening tag must have a closing tag!
	`<tag></tag>`

>**Note:**

> - There are a few exceptions that can be found [here](https://www.quora.com/Which-HTML-tags-are-self-closing/answer/Michael-Dick?srid=XmGB)

----------

**HTML Formatting**

Proper indentation is very important for the readability of your code! Having code that is legible is just as important as having handwriting that is legible, if no one can read it, does it really even exist??

    <grandparent>
    	<parent>
    		<sibling></sibling>
    		<sibling></sibling>
    	</parent>
    </grandparent>

>**Note:**
>
>- Closing tags can end on the same line if there are no children or there is minimal content
>- Closing tags must vertically align with opening tags, so it is clear which belong together

CSS
------

**Embedding CSS**

CSS may be embedded directly into the HTML file if it appears between `script` tags:

`<script></script>`

**Linking to CSS**

Use the self closing `link` tag

`<link rel="stylesheet" href="[RELATIVE PATH TO EXTERNAL STYLESHEET]">`

>**Note**

>- The `rel` attribute is required and specifies the relationship the current document has with the linked document
>- The `<link>` is inserted in the `<head>` tags AFTER the `<title>` tags


**CSS Code Styling**

Proper CSS declarations:

    selector-a {
    	property-a: value-a;
    	property-a: value-a;
    }

    selector-b {
    	property-c: value-c;
    	property-d: value-d;
    }

   >**Note**

>- The properties appear in alphabetical order within the CSS declaration
>- There is a SINGLE space between the selector and opening curly brace `{`
>- The properties and values appear on the next line and they are indented in from the selector
>- There is a SINGLE space between the `:` and the value.
>- Every value ends in a semi-colon `;`
>- The closing curly brace `}` is on its own line, lined up with start of the selector


SCSS
-------

SCSS obeys the same rules as CSS listed above regarding format and style of code. Here is how to incorporate the rules of the new features of SCSS with those basic CSS rules.

**Variables** (used to store information you want to reuse throughout the style sheet)

Defining:

    $variableNameA: variable-property-a;
    $variableNameB: variable-propertyb;

Using:

    selector {
    	property: $variableNameA;
    }

>**Note:**

>- The variable name will always be camelCase
>- The variables will appear at the very top of the stylesheet, before any declarations are made
>- They are in alphabetical order, like the selectors and properties
>- All variable names start with a `$` to indicate to the stylesheet that it is a variable name

**Mixins** (lets you make groups of CSS declarations that you want to reuse throughout your site) think like a bigger variable!

Defining:

    @mixin name-of-rule-a(optional-variable-a) {
    	property-a: optional-variable-a;
    	property-b: value-b
    }

    @mixin name-of-rule-b {
    	property-c: value-c;
    	property-d: value-d;
    }

Using:

    selector-a {
    	@include name-of-rule-a(value-for-optional-variable);
    }

    selector-b {
    	@include name-of-rule-b;
    }

>**Note:**

>- Mixins will appear below variable, but above CSS declarations
>- Defining the mixin always starts with `@mixin` followed by a space and then the name of the declaration
>- If using the optional variable is used it is passed in between parenthesis `()` with NO SPACE after the variable name
>- The rules are then defined like a traditional CSS declaration, including using the curly braces `{}`
>- When using the mixin begin by using `@include` followed by the mixin name within the CSS declaration
>- If using an optional variable pass in the value of that variable after the mixin name between the parenthesis `()`

**SCSS Nesting**

SCSS can include nested declarations in order to get to nested HTML elements

HTML

    <parent-element>
    	<child-element></child-element>
    </parent-element>


Nested SCSS

    parent-element {
    	property-a: value-a;
    	property-b: value-b;

    	child-element {
    		property-c: value-c;
    	}
    }

>**Note:**

>- The SCSS child element is indented, just like the HTML
>- The child element inherits the properties of the parent element
