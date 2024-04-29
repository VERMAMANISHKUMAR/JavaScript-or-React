## Document Object Model (DOM) in JavaScript

### 1. What is DOM?
DOM stands for Document Object Model. It represents the structured content of an HTML document as a tree-like structure where each node represents a part of the document.

### DOM Selectors:
DOM selectors are methods provided by the Document Object Model (DOM) API that allow developers to select and manipulate HTML elements in a web page. There are various methods available to select elements, including:

**1. getElementById:** - Selects an element by its unique ID attribute.
```const elementById = document.getElementById("elementId");```

**2. getElementsByClassName:** - Selects elements by their class name.
```const elementsByClass = document.getElementsByClassName("className");```

**3. getElementsByTagName:** - Selects elements by their tag name.

```const elementsByTag = document.getElementsByTagName("tagName");```

**4. querySelector:** - Selects the first element that matches a specified CSS selector.
```const firstElement = document.querySelector(".selector");```

**5. querySelectorAll:** - Selects all elements that match a specified CSS selector.
```const allElements = document.querySelectorAll(".selector");```

 **NodeList:**

          - Represents a collection of nodes, typically returned by methods like querySelectorAll.
          - It is important to note that NodeList objects are "live", meaning that they are automatically updated when the underlying document structure changes
          - Does not include non-element nodes.
          - Is live, meaning it updates when the DOM changes.
          
+ **HTMLCollection:**
- Represents a collection of HTML elements, typically returned by methods like getElementsByClassName or getElementsByTagName

- Does not include non-HTML elements.
- Contains only HTML elements.
          - Represents a collection of nodes, typically returned by methods like querySelectorAll.
          - Contains only HTML elements.
          - Is not live.

### 2. Modifying NodeList and HTMLCollection

We show that NodeList and HTMLCollection are live, meaning they automatically update when the document structure changes.

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>DOM Selectors</title>
  </head>
  <body>
    <div id="container">
      <p class="para">Paragraph 1</p>
      <p class="para">Paragraph 2</p>
      <p class="para">Paragraph 3</p>
    </div>
    <script>
      // Using DOM selectors
      const container = document.getElementById("container");
      const paragraphsByClass = document.getElementsByClassName("para");
      const paragraphsByTag = document.getElementsByTagName("p");
      const firstParagraph = document.querySelector(".para");
      const allParagraphs = document.querySelectorAll(".para");

      console.log(container); // <div id="container">...</div>
      console.log(paragraphsByClass); // HTMLCollection of all elements with class "para"
      console.log(paragraphsByTag); // HTMLCollection of all <p> elements
      console.log(firstParagraph); // <p class="para">Paragraph 1</p>
      console.log(allParagraphs); // NodeList containing all <p> elements with class "para"

      // Modifying NodeList and HTMLCollection
      container.innerHTML += '<p class="para">Paragraph 4</p>'; // Updates NodeList
      console.log(allParagraphs); // NodeList now contains Paragraph 4
    </script>
  </body>

</html>

**In this example:**
 + We select elements using various DOM selectors.
+ We demonstrate the difference between NodeList and HTMLCollection.
+ We show that NodeList and HTMLCollection are live, meaning they automatically update when the document structure changes.
Understanding these concepts is crucial for effectively manipulating HTML elements in JavaScript.

### DOM Selectors:
**1.getElementById:**

- Selects an element by its unique ID attribute.

```const elementById = document.getElementById("elementId");```

**2. getElementsByClassName:**


- Selects elements by their class name.
```const elementsByClass = document.getElementsByClassName("className");```

**3. getElementsByTagName:**

- Selects elements by their tag name.
```const elementsByTag = document.getElementsByTagName("tagName");```

**4. querySelector:**


- Selects the first element that matches a specified CSS selector.
```const firstElement = document.querySelector(".selector");```

**5. querySelectorAll:**


- Selects all elements that match a specified CSS selector.
```const allElements = document.querySelectorAll(".selector");```

### NodeList vs HTMLCollection:

+ **NodeList:**
- Represents a collection of nodes, typically returned by methods like querySelectorAll.
- It is important to note that NodeList objects are "live", meaning that they are automatically updated when the underlying document structure changes
- Does not include non-element nodes.
- Is live, meaning it updates when the DOM changes.

+ **HTMLCollection:**
- Represents a collection of HTML elements, typically returned by methods like getElementsByClassName or getElementsByTagName
- HTMLCollection is array-like but not a true array (e.g., lacks array methods like forEach).
- Does not include non-HTML elements.
- Contains only HTML elements.
- Represents a collection of nodes, typically returned by methods like querySelectorAll.
- Contains only HTML elements.
- Is not live.

### 3. Differences between NodeList and HTMLCollection

The NodeList and HTMLCollection objects are both collections of nodes, but they differ in their behavior.
 

Here's a summary with code examples:

// Using DOM selectors
```const elementById = document.getElementById("elementId");```
```const elementsByClass = document.getElementsByClassName("className");```
```const elementsByTag = document.getElementsByTagName("tagName");```

```const firstElement = document.querySelector(".selector");```

```const allElements = document.querySelectorAll(".selector");```

// NodeList
```console.log(allElements); // NodeList```

// HTMLCollection
```console.log(elementsByClass); // HTMLCollection```

Understanding these differences is important for choosing the appropriate method based on your requirements and efficiently manipulating DOM elements in JavaScript.

textContent, innerHTML, and innerText are properties used to manipulate the content of HTML elements. Here's a breakdown of each:

**1. textContent:**

- **Description:** Represents the text content of a node and all its descendants. It returns the text content as a string, including all nested elements.
- **Usage:**
```const element = document.getElementById("example");```
```console.log(element.textContent); // Retrieves the text content```
```element.textContent = "New text"; // Sets the text content```

**2. innerHTML:**


- **Description:** Represents the HTML content of the element. It allows you to retrieve or set the HTML markup inside the element, including any nested elements.
- **Usage:**
```const element = document.getElementById("example");```
```console.log(element.innerHTML); // Retrieves the HTML content```
```element.innerHTML = "<strong>New HTML</strong>"; // Sets the HTML content```

**3. innerText:**


- **Description:** Represents the rendered text content of the element. It returns the visible text content, excluding any hidden or non-visible elements (like <script> or <style> elements).
- **Usage:**

```const element = document.getElementById("example");```
```console.log(element.innerText); // Retrieves the rendered text content```
```element.innerText = "New text"; // Sets the rendered text content```

**Note:** It's important to be cautious when using innerHTML, as setting it with user-generated content can lead to security vulnerabilities like cross-site scripting (XSS) attacks. Use textContent when manipulating text content to avoid these issues unless you specifically need to handle HTML markup.

Here's an example that demonstrates the use of these properties:

```<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>textContent vs innerHTML vs innerText</title>
  </head>
  <body>
    <div id="example">
      <p>Hello, <strong>world</strong>!</p>
    </div>

    <script>
      const element = document.getElementById("example");

      console.log(element.textContent); // Outputs: "Hello, world!"
      console.log(element.innerHTML); // Outputs: "<p>Hello, <strong>world</strong>!</p>"
      console.log(element.innerText); // Outputs: "Hello, world!"

      // Modifying content
      element.textContent = "New text"; // Sets textContent
      element.innerHTML = "<strong>New HTML</strong>"; // Sets innerHTML
      element.innerText = "New text"; // Sets innerText
    </script>
  </body>
</html>```