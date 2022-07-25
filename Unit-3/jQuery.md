<div align="center">

[**_``Go Back``_**](../README.md)

# JQuery

</div>

## Introduction

``jQuery`` is a lightweight, ``write less, do more``, JavaScript library.

The purpose of ``jQuery`` is to make it much easier to use ``JavaScript`` on your website.

``jQuery`` takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.

``jQuery`` also simplifies a lot of the complicated things from ``JavaScript``, like ``AJAX`` calls and ``DOM`` manipulation.

The ``jQuery`` library contains the following features:

- ``HTML/DOM`` manipulation
- ``CSS`` manipulation
- ``HTML`` event methods
- Effects and animations
- ``AJAX``
- Utilities

## Playing With Elements

### **jQuery Selectors**

jQuery selectors allow you to select and manipulate HTML element(s).

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing CSS Selectors, and in addition, it has some own custom selectors.

All selectors in jQuery start with the dollar sign and parentheses: ``$()``.

#### **The element Selector**:
The jQuery element selector selects elements based on the element name.

You can select all ``<p>`` elements on a page like this:

```JS
$("p")
```

#### **The #id Selector**:
The jQuery ``#id`` selector uses the id attribute of an HTML tag to find the specific element.

An id should be unique within a page, so you should use the ``#id`` selector when you want to find a single, unique element.

To find an element with a specific id, write a hash character, followed by the id of the HTML element:

```JS
$("#test")
```


#### **The .class Selector**:
The jQuery ``.class`` selector finds elements with a specific class.

To find elements with a specific class, write a period character, followed by the name of the class:

```JS
$(".test")
```

### **JQuery Event** 

In jQuery, most DOM events have an equivalent jQuery method.

To assign a click event to all paragraphs on a page, you can do this:

```JS
$("p").click();
```

The next step is to define what should happen when the event fires. You must pass a function to the event:

```JS
$("p").click(function(){
  //action goes here!!
});
```

|Mouse Events|Keyboard Events|Form Events|Document Events|
|------------|---------------|-----------|---------------|
|click       |keypress       |submit     |load           |
|dblclick    |keydown        |change	   |resize         |
|hover       |keyup	         |select	   |scroll         |
|mousedown   |blur           |unload     |               |
|mouseup     |focusin        |ready      |               |

### **JQuery Attributes**

``jQuery`` is being heavily used in manipulating various attributes associated with HTML elements. Every HTML element can have various standard and custom attributes (i.e. properties) which are used to define the characteristics of that HTML element.

jQuery gives us the means to easily manipulate (Get and Set) an element's attributes. First let's try to understand a little about HTML standard and custom attributes.

Standard Attributes
Some of the more common attributes are −

- className
- tagName
- id
- href
- title
- rel
- src
- style

## jQuery UI

JqueryUI is a powerful Javascript library built on top of jQuery JavaScript library. UI stands for User interface, It is a set of plug-ins for jQuery that adds new functionalities to the jQuery core library.

The set of plug-ins in JqueryUI includes interface interactions, effects, animations, widgets, and themes built on top of jQuery JavaScript Library.

It was released in September 2007, announced in a blog post by John Resig on jquery.com. The latest release, 1.10.4, requires jQuery 1.6 or later version. jQuery UI is a free, open source software, licensed under the MIT License.

The below are some of the benefits of Jquery UI −

- Cohesive and Consistent APIs.
- Comprehensive Browser Support.
- Open Source and Free to Use.
- Good Documentation.
- Powerful Theming Mechanism.
- Stable and Maintenance Friendly.