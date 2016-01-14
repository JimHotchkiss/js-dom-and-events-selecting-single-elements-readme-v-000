# The DOM

## Objectives
+ Explain what the DOM is
+ Explain the DOM hierarchy
+ Explain how to access the DOM with JavaScript

## Intro
Let's think about Gmail for a second. When you're looking at your inbox, there are a million actions you can take. You favorite an email and the star turns yellow without a new page loading. You add a tag to an email and the tag also appears without the page reloading. Even opening an email just replaces the inbox content with the email content without loading a new page. All of this is done using JavaScript and jQuery. But how was the code able to manipulate the HTML? By using traversing and manipulating the DOM.


DOM, which stands for Document Object Model, is an API for manipulating HTML and XML documents. It provides a structural representation of the document in tree form, enabling you to modify its content and visual presentation by using a scripting language such as JavaScript.

## The Tree

![Dom Structure Tree](https://s3.amazonaws.com/learn-verified/dom-tree.gif)

+ **Window**
  + The highest level of the DOM tree is the window object. Think of the window as the browser window. The window contains the entire DOM document. All components of your HTML file will be accessible from within the window.
  + The window object has a large number of properties that return information about the object. Below are a few examples

```js
window.document;
//returns the entire HTML document

window.innerWidth;
// returns the inner width of the browser window. Open a console in the browser and enter this. Then shrink the browser window and run it again. You should get a different value.

window.innerHeight;
// returns the inner height of the browser window.
```

+ **Document**  
  + The document object represents any web page loaded in the browser. The document contains all the nodes that represent the HTML elements of the page. We use the document object to traverse through the HTML and manipulate elements.
  + There are many document properties that allow us to obtain information about the document programmatically.

```js
document.all;
// returns all the nodes inside the document object

document.contentType;
// returns the type of content contained. Most web pages should return "text/html"

document.URL;
// returns the URL of the document object
```

Below the document, are all the nodes representing the HTML or ZML elements on the page.

## Altering The DOM

We can alter the DOM through several different ways:

+ Add/remove/hide/show HTML elements in the page.
+ Add/remove/change HTML attributes.
+ Add/remove/change  CSS styles.
+ Listen for key presses or mouse events upon Elements
+ Create events in the page.

## Selecting Elements

We can select HTML elements in the document with JavaScript and jQuery:

JS:
```js
document.getElementByTagName("p");
//returns all p tags on a page
```

jQuery:
```js
$("p");
```

The DOM will become increasingly important as we use JavaScript and jQuery to manipulate our sites.

## Resources

+ [MDN DOM Introduction](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
+ [W3C Schools Window Properties](http://www.w3schools.com/jsref/obj_window.asp)
+ [MDN Document Properties](https://developer.mozilla.org/en-US/docs/Web/API/Document)
