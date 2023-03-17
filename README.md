## Exercise 1: Creating a webpage with semantic HTML

In this exercise, you will create a webpage using semantic HTML. The webpage should have a navbar, content, and sidebar, with different background colors.
1. Open the index.html file on your text editor and browser;
2. Observe the semantic HTML elements to structure the webpage: nav for the navbar, main for the content, and aside for the sidebar.
3. Complete the HTML and CSS code in order to replicate the following image:




## Exercise 2: Displaying a list of items in a list format
In this exercise, you will wrap the main content in a list format on the webpage created in Exercise 1. 
Hints:
- Add a ul element inside the main element.
- Add li elements inside the ul element for each item in the list.
- Use img tags to display images for each item.

The final result should look like the following image:


## Exercise 3: Using flexbox to make the list responsive
In this exercise, you will use flexbox to make the list responsive on different screen sizes.
Hints:
    - Use CSS styles to set display: flex on the ul element.
    - Use flex-wrap to control how the items wrap when the screen size changes.


## Exercise 4: Using CSS Grid to make the list responsive
In this exercise, you will refactor the webpage in order to replace flexbox with CSS Grid to make the list responsive on different screen sizes.

Hints:
  - Use CSS styles to set display: grid on the ul element.
  - Use grid-template-columns to define the grid columns.
  - Use grid-gap to control the spacing between the items.

## Exercise 5: Using JavaScript to add content to the list dynamically
In this exercise, you will use JavaScript to add content to the list dynamically.

1. Add a form element below the current content of the webpage.
2. Add input fields for the item text and image URL.
3. Add a button to submit the form.
4. Use pure JavaScript to add a new item to the list when the button is clicked

Hint: 
- Use DOM functions to dinamically get the form data, create a new list item and respective elements and insert it on the list.
- https://www.w3schools.com/jsref/event_onsubmit.asp

````
    // Function to handle form submission
    function handleSubmit(event) {
        // Prevent the form from submitting normally
        event.preventDefault();

        // Get the input values
        const image = document.getElementById("image-input").value;
        // ...

        // Create a new list item element
        const newItem = document.createElement("li");

        // Create a new image element
        const newImage = document.createElement("img");
        newImage.src = image;
        // ...
        newItem.appendChild(newImage);

        // Create the text node and add it to the list item
        // TODO        

        // Add the new list item to the list
        // TODO

        // Reset the form
        //TODO
    }
````

# Exercise 6: Creating the webpage with React
In this exercise, you will use React to create the webpage created in Exercise 1.

1. Install the create-react-app package using npx create-react-app my-app.
2. Add the previous CSS file content to the App.css file.
3. Remove the template code inside the div classname="App" in the App.js file. 
3. Create a components directory in the src folder.
4. Create a new component for the main HTML elements from the exercise 1. 
5. Import and place the components on the App component.

Hints: 

Header component (componentes/Header.js):
````
import './../App.css'; 


const Header = (props) => {
    return (
      <header>
        <h1>{props.head_text}</h1>
      </header>
    );
  }

export default Header;

````

App.js:

```
...
import Header from './components/header';

function App() {
  return (
    <div className="App">
       <Header head_text="Porto Legends"/>
    </div>
  );
}
...
```