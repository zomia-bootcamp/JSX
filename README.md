# JSX

## Understanding the Code: JavaScript and JSX

Take a look at the following line of code:

```jsx
const h1 = <h1>Hello world</h1>;
```

You might be wondering what kind of strange code this is. Is it JavaScript? HTML? Or something else entirely?

### Expirement

Copy the following line into [index.html](./index.html):

```jsx
const h1 = <h1>Hello world</h1>;

```
What are you expecting to see in the browser?


Now, drag the file to an empty browser. Was you guess right?
What is going on??


## Unveiling the Mystery

The answer may surprise you—it belongs in a JavaScript file! Although it resembles HTML, the code you shared doesn't actually contain any HTML elements.

The part that resembles HTML, `<h1>Hello world</h1>`, is known as JSX. JSX is a syntax extension used in React to write HTML-like code within JavaScript.

Even though it looks like HTML, the code is meant to be written and executed in a JavaScript environment, particularly when using React. If you attempted to run this code in a plain HTML file, it wouldn't work as expected.

So, the mystery is unveiled: the code snippet combines JavaScript and JSX, where JSX allows us to write HTML-like syntax within JavaScript for React development.

## Understanding JSX: A Syntax Extension for JavaScript

JSX is a syntax extension for JavaScript that was specifically created to be used with React. It allows developers to write code that closely resembles HTML within their JavaScript files.

But what exactly does "syntax extension" mean?

In this context, a syntax extension refers to the fact that JSX is not valid JavaScript on its own. Web browsers are unable to interpret and execute JSX code directly.

To overcome this, when a JavaScript file contains JSX code, it needs to go through a process called compilation. During compilation, a JSX compiler translates the JSX code into regular JavaScript that can be understood and executed by web browsers.

## Installing React
### Exercises

To compile our jsx, wew will need to install react on our project. To do so, visit the OpenAI ChatGPT interface. Simply ask a question like, "Can you provide instructions on installing a React app?" ChatGPT will then respond with detailed guidance on how to proceed. Remember that React is necessary to compile JSX code, which allows you to write HTML-like syntax within your React components. If you encounter any issues or need further clarification, feel free to ask ChatGPT for additional information or assistance. Follow the instructions provided by ChatGPT to successfully install your React app.

**Before you move on:** 
Run the following command to check the installed version of React in your project:
```
npm list react
```
This command will display the version of React installed in your project along with its dependencies. If React is not installed, you will see an error message.


## JSX Elements: Building Blocks of JSX

In JSX, the fundamental building block is called a JSX element. Let's take a look at an example of a JSX element:

```jsx
<h1>Hello world</h1>
```

Despite the visual resemblance to HTML syntax, it's important to understand that **JSX is not actually HTML**. It is a syntax extension for JavaScript that allows developers to write HTML-like code within their JavaScript files, particularly when working with React.

JSX elements represent the structure and content of a user interface component. They can be used to create complex UI hierarchies by nesting JSX elements within one another. These elements can include tags, attributes, and content, just like in HTML.

It's worth noting that when the JavaScript file containing JSX code is compiled, the JSX elements are translated into regular JavaScript code for execution by the web browser.

### Exercises

In app.js, write a JSX `<p>` element containing the text, `Hello world`. Use the example code above as a guide.


## JSX Elements and Their Usage in JavaScript

JSX elements are treated as JavaScript expressions, which means they can be used in various ways just like any other JavaScript expression. They are not limited to HTML-like syntax.

Here are a couple of examples showcasing the usage of JSX elements in different scenarios:

Example 1: Saving a JSX element in a variable:
```jsx
const navBar = <nav>I am a nav bar</nav>;
```

In this case, the JSX element `<nav>I am a nav bar</nav>` is assigned to the variable `navBar`. This allows us to reuse the JSX element later in the code.

Example 2: Storing JSX elements in an object:
```jsx
const myTeam = {
  center: <li>Benzo Walli</li>,
  powerForward: <li>Rasha Loa</li>,
  smallForward: <li>Tayshaun Dasmoto</li>,
  shootingGuard: <li>Colmar Cumberbatch</li>,
  pointGuard: <li>Femi Billon</li>
};
```

In this example, we have an object called `myTeam` that contains multiple JSX elements, each assigned to a specific key. This demonstrates how JSX elements can be stored within objects for organizational purposes.

These examples illustrate the versatility of JSX elements, as they can be assigned to variables, passed as function arguments, stored in data structures like objects or arrays, and used in various other JavaScript expressions.

### Exercises

In app.js, create a JSX `<article>` element. Save it in a variable named myArticle. 


## Attributes in JSX: Adding Information to JSX Elements

Similar to HTML elements, JSX elements can also have attributes to provide additional information or configuration. The syntax for writing JSX attributes resembles HTML:

```jsx
my-attribute-name="my-attribute-value"
```

Here are a few examples of JSX elements with attributes:

```jsx
<a href='http://www.example.com'>Welcome to the Web</a>;

const title = <h1 id='title'>Introduction to React.js: Part I</h1>;

const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px'>;
```

In the first example, the anchor (`<a>`) element has an `href` attribute that specifies the URL to link to.

The second example demonstrates a heading (`<h1>`) element with an `id` attribute, which can be used to uniquely identify the element.

Lastly, the image (`<img>`) element showcases multiple attributes: `src` specifies the image file path, `alt` provides alternative text for accessibility, and `width` and `height` determine the dimensions of the image.

Just like HTML, JSX elements can have multiple attributes, allowing you to provide various details or configure the element as needed.

### Exercises

In app.js, Declare a constant named `p1`.

Set `p1` equal to a JSX `<p>` element containing the text `foo`.

On the next line, declare a constant named `p2`.

Set `p2` equal to another JSX `<p>` element containing the word `bar`.

Give the `<p>` stored in `p1` an `id` attribute of `'large'`.

Give the `<p>` stored in `p2` an `id` attribute of `'small'`.


## Nested JSX: Creating Hierarchical JSX Structures

In JSX, just like in HTML, you can nest JSX elements inside other JSX elements, forming a hierarchical structure.

Here's an example of a JSX `<h1>` element nested inside a JSX `<a>` element:

```jsx
<a href="https://www.example.com"><h1>Click me!</h1></a>
```

To improve readability, you can use HTML-style line breaks and indentation:

```jsx
<a href="https://www.example.com">
  <h1>
    Click me!
  </h1>
</a>
```

When a JSX expression spans multiple lines, it's important to wrap the multi-line JSX expression in parentheses:

```jsx
(
  <a href="https://www.example.com">
    <h1>
      Click me!
    </h1>
  </a>
)
```

Nested JSX expressions can be assigned to variables, passed as function arguments, or used in any other way that non-nested JSX expressions can. Here's an example of a nested JSX expression saved as a variable:

```jsx
const theExample = (
  <a href="https://www.example.com">
    <h1>
      Click me!
    </h1>
  </a>
);
```

By leveraging nested JSX, you can create complex and structured JSX components to build dynamic and interactive user interfaces in React.

### Exercises

Declare a new variable named myDiv. Set myDiv equal to a JSX <div> element.

Wrap the <div></div> in parentheses, and use indentation and line breaks like in the examples. In between the <div></div> tags, nest an <h1></h1> containing the text Hello world.

  
## JSX Outer Elements: The Rule of Having a Single Outermost Element

There is an important rule in JSX that we haven't mentioned yet: **a JSX expression must have exactly one outermost element.**

Let's illustrate this rule with an example:

```jsx
// Which example is valid jsx?

const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);


const paragraphs = (
  <p>I am a paragraph.</p> 
  <p>I, too, am a paragraph.</p>
);
```

In the first example, the JSX expression has a single outermost element, which is the `<div>` element. Inside the `<div>`, we have two `<p>` elements.

However, the second example violates the rule. It tries to have two outer elements, two `<p>` elements without being wrapped in another element. This is not allowed in JSX.

If you encounter a situation where your JSX expression has multiple outer elements, the solution is straightforward: wrap the entire JSX expression in a `<div>` element (or any other suitable wrapper element).

By ensuring that your JSX expression has a single outermost element, you can avoid errors and ensure that your JSX code is valid and well-structured.
  

### Exercises
  
  Follow the instructions in [blog.js](./exercises/blog.js)
  
  
## Rendering JSX: Bringing JSX to the Screen

You’ve learned how to write JSX elements! Now it’s time to learn how to render them.

To render a JSX expression means to make it appear on screen.
  

### Exercises
  
Open the `index.js` file and read the code carefully.
  
  
## Rendering JSX Explained: Content and Placement

To understand the code provided in `index.js`, it's important to grasp two key concepts in React rendering: the **content** to render and the **placement of that content**.

Let's break down the code:

1. **Importing Dependencies**: The first step is to import necessary dependencies and files. The `import` statements at the beginning of the file import the required modules and files for the React application. This includes the `React` library, `ReactDOM` from the React library, stylesheets, the main component (`App`), and any other utility functions or components needed.

2. **Root Element Setup**: In the next step, a root element is created to serve as the entry point for the React application. This is done using the `ReactDOM.createRoot` method, which takes the element with the ID of `'root'` from the HTML document as an argument. This is the element where the React application will be rendered.

3. **Rendering the App Component**: The `root.render` method is used to render the main component (`App`) inside the root element. This method takes the component as an argument and renders it within the root element. In the provided code, the `App` component is wrapped in `<React.StrictMode>`. This is a development mode feature that performs additional checks and warnings to help identify potential issues.

4. **Performance Measurement (Optional)**: The last line of code calls the `reportWebVitals` function. This function is typically used for measuring and reporting performance metrics in the application. Depending on the implementation, it can log the results to the console or send them to an analytics endpoint. This line is optional and can be removed if performance measurement is not required.

To guide a beginner developer through this code, you can explain the purpose of each step and its significance in a React application:

1. Explain that the `index.js` file serves as the entry point for the React application and is responsible for rendering the main component (`App`) into the DOM.

2. Point out the `import` statements and explain that they bring in necessary dependencies and files for the application to work correctly. Emphasize the importance of importing the required modules and files before using them in the code.

3. Describe the concept of a root element and its role in rendering the React application. Explain that the `createRoot` method is used to create a root element, and the `render` method is used to render the main component (`App`) inside it.

4. Mention the optional `reportWebVitals` function and its purpose in measuring and reporting performance metrics. Explain that it can help identify areas for improvement in the application's performance.

### Exercises
  
Now that you understand what is going on, add comments in `index.js` that will break down the code according to the explanation above.
  
  
  
  
  
# Why React?

React.js is a JavaScript library developed by engineers at Facebook. Here are some compelling reasons why React has become a top choice for web development:

## 1. Speed and Performance
React is known for its fast performance. It efficiently handles complex updates and ensures that apps remain quick and responsive. This makes it suitable for building high-performing web applications.

## 2. Modularity
One of the key advantages of React is its modular approach to development. Rather than writing large, monolithic code files, React encourages developers to create smaller, reusable components. This modularity not only improves code maintainability but also enhances developer productivity.

## 3. Scalability
React shines when it comes to handling large-scale applications with a lot of dynamically changing data. Its virtual DOM (Document Object Model) allows for efficient rendering and updates, ensuring smooth performance even with extensive data manipulation.

## 4. Flexibility
React's versatility extends beyond web application development. Developers can utilize React for various projects, exploring its potential beyond traditional web development. Its component-based architecture and robust ecosystem offer flexibility and room for innovation.

## 5. Popularity and Employability
React has gained immense popularity in the developer community. Understanding React and gaining proficiency in it can significantly enhance your employability. As React continues to be widely adopted, having React skills can open up numerous job opportunities in the web development industry.

Whether you are new to React or an experienced developer, the library's simplicity and ease of use make it accessible to all. By starting with the basics and gradually diving into advanced concepts, you can gain a solid understanding of React and unleash its potential for creating powerful web applications.

