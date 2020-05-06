# Questions


1. Review 1.2 for in loop practice problem?
   - Objects are composed of properties (keys) and property values (key values).
   - In a for in loop, we declare a placeholder value that will represent the **property**, not the property value. We then can use bracket notation and the declared variable to access the property value.
   ```js
   const john = {
      firstName: 'John',
      lastName: 'Redd',
      hobby: 'Programming'
   }

   for ( let prop in john ) {
      console.log(prop) // The variable representing the property
      console.log(john[prop]) // How we use that variable to access the property value
   }
   ```

2. Review the DOM generally and maybe draw out how the different things are talking to each other? 

   - The Document Object Model (DOM) connects web pages to scripts or programming languages by representing the structure of a document—such as the HTML representing a web page—in memory. [MDN DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
   - Essentially the DOM is an object representation of your html file that we can access in JavaScript through the `document`. It includes methods that allow us to target more specific parts and elements of the html file.

3. Define an element node and how it is different from normal javascript arrays or functions? Go over how an element ties in?

   - An element node is just a JavaScript Object representing an html element and all it's different attributes.

4. Talk more about how to see parent/child relationships in HTML and then how CSS selects those to make modifications?

   - Formatting the HTML doc will help with seeing the parent child relationships.
   - CSS Selectors will be in the style.css file at the bottom

5. Go over the different kinds of tags in HTML, when they're used, organization strategies etc.?

   - Content Tags: h1 - h6, img, p, etc.
   - Interactive Tags: input, button, etc.
   - Container Tags: div, section, header, footer, nav, etc.
     - Use these to group other tags together for flex box and other layout purposes.

6. Object destructuring afternoon project

   - Shorthand, saves us from object drilling
  ```js
  /* Disclaimer - None of this will run in repl or anywhere else because I have reused propertyName as a var multiple times in this one file. */

  const obj = {
     propertyName: 'Hello World',
     propOne: 1,
     propTwo: 2
  }

  // Functionally these are both the same.
  const propertyName = obj.propertyName // Not object destructuring
  const { propertyName } = obj // Object Destructuring

  // One advantage of object destructuring is the following.
  const { propertyName, propOne, propTwo } = obj; // I can get all the props I want off in one go.

  // Whereas doing this, I end up having to repeat myself a lot.
  const propertyName = obj.propertyName;
  const propOne = obj.propOne;
  const propTwo = obj.propTwo;
  ```

7. What is returned by each of the node targets that we went over in lecture today? Like do they return arrays, strings, objects in arrays etc?

   - Nodes are always objects. But depending on the selector method we use, we can get back either one object, or an array of objects
  ```js
  const divs = document.querySelectorAll('div');
  console.log(divs); // This will be an array of objects, each object within the array is a JavaScript representation of all my div tags in my html file.

  const favoriteDiv = document.getElementById('favorite-div');
  console.log(div) // This will be an object, a JavaScript representation of my div with the id of favorite-div that is in my html file.
  ```

8. Go over our morning review from HTML-CSS 2? It was the one with the Owen Wilson facebook post? It's found here https://github.com/andrewwestenskow/morning-reviews/tree/master/week2/fbPostPractice

   - See index.html and style.css