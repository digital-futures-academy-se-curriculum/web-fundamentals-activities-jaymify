# Manipulating Styles with JavaScript

## Objectives

- To be able to and examine and manipulate CSS styles using JavaScript.

## Activity
1. In VSCode, open the file `index.js` from the `starter/src` folder.
2. Open VSCode’s in-built console by selecting View -> Integrated Terminal (or use the shortcut key or icon on the bottom bar).
3. Ensure that you have the Live-Server VSCode extension installed
4. When installed, right click on the index.html file and select Open with Live Server option - this should open the browser with the page.

The browser window will open, but there will be nothing to view except the provided code!
The are 3 lines of code already provided.  These are to enable the buttons on the webpage to work when clicked.

5. Under the provided lines of code but before the `blueToRed` function, declare a **constant** called `blueParagraph` and set this to be the element that has the **id** `blueParagraph`.
6. `console.log` the color obtained from its style object.
7. `console.log` the color obtained from the result of running it through `getComputedStyle` function:

```js
console.log(getComputedStyle(blueParagraph).color);
```

8. Populate the function `blueToRed` with code that:

    a. Sets the `color` value in the style object to `red`;
    b. Logs out the new value of the `color` from the style object;
    c. Logs out the value of `color` from the ```getComputerStyle``` function;
    d. Sets `blueParagraph`'s `textContent` to be its own value when it has the `replace` function applied to it to remove `'blue'` and replace it with `'red'`;

```js
blueParagraph.textContent = blueParagraph.textContent.replace('blue', 'red');
```

9. Save the file and check that the page behaves as expected.
 
You should notice that there are blank lines on the console where the `style.color` value should be from the first call.  This is because the `style.color` is `undefined` as it has been set by a CSS class.  When the button is clicked, `red` and the `rgb` value are printed as the `color` value has been set in-line.

10. Immediately after the `blueToRed` function, declare a **constant** called `greenParagraphs` and set this to be an array of elements with `class` `greenBg` applied to them.
11. Log out the `style.backgroundColor` and the *computed style background colour* of the first element in the array:

```js
console.log(greenParagraphs[0].style.color);
console.log(getComputedStyle(greenParagraphs[0]).color);
```

12. Populate the greenToPink function with a for…of loop that takes each greenParagraph of greenParagraphs and:
    
    a. Sets the `className` of `greenParagraph` to `hotpinkBg`;
    b. Logs out the `backgroundColor` from the style object and the `getComputedStyle` function
    c. Sets `greenParagraph`'s `textContent` to be its own value when it has the replace function applied to it to remove `'green'` and replace it with `'pink'`;

13. Save the page and observe the results when the button is clicked.
    
The value for `backgroundColor` from the style object is missing initially and when the button is clicked here because, in both cases, the value is set by a CSS class.

14. Immediately after the `greenToPink` function, declare a **constant** called `tnrParagraph` and set this to be the element with an **id** of `tnrParagraph`.
15. Log out the `style.fontFamily` value and the *computed* `fontFamily`.
16. Populate the `tnrToArial` function with code that:
    
    a. Sets the `style.fontFamily` to `arial`;
    b. Logs out the `style.fontFamily` value and the *computed* fontFamily;
    c. Sets `tnrParagraph`'s `textContent` to be its own value when it has the `replace` function applied to it to remove `'Times New Roman'` and replace it with `'Arial'`;
    d. Sets `textContent` of `greenParagraph` to `newText`.
    
17.	Save the file and check that it behaves as expected. 
