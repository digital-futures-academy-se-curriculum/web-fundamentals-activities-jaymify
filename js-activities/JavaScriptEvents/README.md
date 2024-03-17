# Manipulating Styles with JavaScript

## Objectives

- To be able to add and remove JavaScript events.
  
## Activity
1. In VSCode, open the file **index.js** from the `starter/src` folder.
2. Open VSCode’s in-built console by selecting View -> Integrated Terminal (or use the shortcut key or icon on the bottom bar).
3. Ensure that you have the Live-Server VSCode extension installed
4. When installed, right click on the index.html file and select Open with Live Server option - this should open the browser with the page.

The browser window will open, but there will be nothing to view except the provided code!

5. Under the comment, add event listeners to the elements, using the functions shown:

| ELEMENT                       | EVENT   | HANDLER       |
| ----------------------------- | ------- | ------------- |
| BUTTON WITH ID OF TEXTCONTENT | `click` | `blueToRed`   |
| BUTTON WITH ID OF BGCOLOUR    | `click` | `greenToPink` |
| BUTTON WITH ID OF FONTS       | `click` | `tnrToArial`  |

6. Save the file and make sure that the page functions as it did at the end of **Manipulating Styles**.
7. Add an event listener to `tnrParagraph` that has an event of `mouseover` and a handler of `mouseOver`.
8. Add `mouseOver` as an *arrow function* that takes an argument of event:

```js
const mouseOver = event => { 
	// function body here
}
```

9. Populate the function body:

    a. Change the *background colour* of the event target to `limegreen`;

    ```js
    event.target.style.backgroundColor = 'limegreen';
    ```

    b. Check to see if the `textContent` of the *event target* contains the word `background`
        i) If it doesn't then add I have had my background colour changed on mouse over to it;
        ii)	If it does then replace the word out with over in it.

10. Save the page and check to see if the new mouse over functionality works.
    
You should find that it doesn't.  The explanation for this is in JavaScript's hoisting rules.  Normal variables and functions are hoisted by JavaScript, meaning that it knows about them and their implementation no matter where they are declared.  Arrow functions (and Classes - when using Object Oriented JavaScript) are not.  Therefore, the page fails silently.

11. Move the registering of the event listener to beneath the declaration of the arrow function.
12. Save the file and you should see that the event now fires correctly.
13. Add another event handling function to `tnrParagraph`, using the previous steps as a template, to change the background colour to `yellow` when the mouse leaves the element and add/change the text accordingly - don’t forget to register the event on `tnrParagraph`!
 
The way that these new event handlers have been written means that they are reusable across any elements as they are not tightly bound to the element.  When we pass in the event, `event.target` gives the reference to the element which fired the event.

14. Add an arrow function called `elementClick`.  It should:
    
    a. Receive `event` as an argument;
    b.Set the background colour of the element that raised the event to `white`;
    c. Change the text content of the element that raised the event to `I have no event listeners attached to me now`;
    d. Remove the `click` event listener on the button with id of `fonts`;
    e. Remove the `click`, `mouseover` and `mouseout` event listeners from the element that raised the event;
    f. Check the `id` of the element that raised the event and if it was `tnrParagraph`:
        i)	Changes the `textContent` of `blueParagraph` to `Event listeners enabled`;
        ii)	Adds event listeners to `blueParagraph` for `click`, `mouseover` and `mouseout`.
    g. If the element that raised the event didn't have an id of `tnrParagraph` it should:
        i)	Change the `textContent` of `tnrParagraph` to `Event listeners enabled`;
        ii)	Adds event listeners to `tnrParagraph` for `click`, `mouseover` and `mouseout`.

15. Register the click event and handling function with tnrParagraph.
16. Save the file and check that all of the events are fired at the appropriate time.  Use the developer tools and add console.logs if you wish to examine further. 
