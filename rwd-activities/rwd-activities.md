# Web Fundamentals - RWD Quick Labs

## Quick Labs Environment Set-Up

1. Open **VSCode**.
2. Using **File** → **Open** , navigate to the **Quick Labs** folder and click **Open**. This will give
    you access to all of the Quick Lab files and solutions needed to complete the Quick
    Labs.
3. At the bottom of the **VSCode** window, you should see a **Go Live** icon. Click on this
    will launch **live-server** for the currently selected file or folder. If a folder is selected,
    this will be shown in your browser and you will be able to navigate here. If a file is
    selected, the browser will attempt to display the file.

---

## Quick Lab 11 - Media Queries

### Objectives - Quick Lab 11

- Use media queries to change the layout on screen dependent on its size

### Activity 11

1. Open the files **index.html** from the **QuickLabs/ 11 _MediaQueries/starter** folder in
    the browser using **live-server** _(Please see step 3 of setting up the environment for help_
    _on this)_.
2. In **mediaqueries.css** , add a media query that:
   - Detects if the minimum width of the screen is 794 pixels
   - Sets the **body** to have properties of:
       - background with HSLA values of 240, 100%, 50% and 0.
       - margins top and bottom of 25px
       - margins left and right of 6%
   - Sets the **figure** to have properties of:
       - float to be left
       - width to be 40%
       - right margin to be 4.5%
3. Add a second media query that:
   - Sets the **body** to have properties of:
       - background with HSLA values of 120 , 100%, 50% and 0.
       - margins top and bottom of 25px
       - margins left and right of 10 %
       - a maximum width of 1130px
   - Sets the **figure** to have properties of:
       - width of 28%
       - right margin to be 2.5%
4. Check the output in the browser - everything does not work as it should...

Can you work out what is missing from the **index.html <head>**? Think VP!

> This is the end of QuickLab 11

---

## Quick Lab 12 - Grids

### Objectives - Quick Lab 12

- To apply classes to HTML to utilise a Grid layout

### Activity 12

1. Open the files **index.html** from the **QuickLabs/1 2 _Grids/starter** folder in the
    browser using **live-server** _(Please see step 3 of setting up the environment for help on_
    _this)_.
2. Open **grids.css** and examine the style rules that have been placed in the file already.
3. You should apply the appropriate CSS classes to the elements in the HTML to make
    your page (when full-screen) look like the image below:

> For reference, the menu links are 1/4 of the screen.

4. Once you have succeeded, experiment using the other col-X settings.

> This is the end of QuickLab 12

---

## Quick Lab 13 - Flex Box

### Objectives - Quick Lab 13

- To examine some of flexbox's properties and values

### Activity 13

1. Open the files **index.html** from the **QuickLabs/12_Grids/starter** folder in the
    browser using **live-server** _(Please see step 3 of setting up the environment for help on_
    _this)_. Have a look at the output.
2. Examine the CSS classes that are applied to the 3 <ul> tags - you should notice that
    each has a **flex-container** class and then another.
3. In **flexbox.css** create a rule for the **flex-container** _class_ that has:

- **padding** and **margin** set to **0** ;
- **list-style** set to **none** ;
- A **border** that is a **solid** line of **1px** coloured **silver** ;
- **display** set to **flex**.

4. Create a rule for the **nowrap** class that has **flex-wrap** set to **nowrap**.
5. Create a rule for the **wrap** class that has **flex-wrap** set to **wrap**.
6. Create a rule for the **wrap-reverse** class that has **flex-wrap** set to **wrap-reverse**.

Save the file and check the output and that it responds appropriately when you
shrink/expand the size of the available screen.

7. Create a rule for the **direction** class that has **flex-direction** set to **column**.

Again, save and check the output - _the 4th set of blocks should have been affected_.

8. Change the **flex-direction** for the direction class to **row**.
9. Add a rule for the **justify** class and set **justify-content** to **center**.

Again, save and check the output - _the 4th set of blocks should have been affected_.

Experiment with any of the flex properties by adding properties to the classes. Note that
some properties will not affect elements with particular others applied to them.

> This is the end of QuickLab 13

---

## Quick Lab 14 - Responsive Images

### Objectives - Quick Lab 14

- To be able to use the **srcset** attribute with images.
- To use the **<source>** element and **sizes** attributes for responsive images

### Activity 14

1. Open the files **index.html** from the **QuickLabs/11_MediaQueries/starter** folder in
    the browser using **live-server** _(Please see step 3 of setting up the environment for help_
    _on this)_.
2. In the first **<article>** , add an **<img>** that:

- Initially uses the image **"baboon1x.jpg"** as its **src** ;
- Has an **alt** of **"Baboon"** ;
- Has a **srcset** set to **"baboon1x.jpg 1x, baboon2x.jpg 2x"**.

3. Save the file and view in the browser - the _1x image_ should be shown
4. Use the _Device Selector_ in the _Developer Tools_ and **reload** the page. This should
    change the image to the _2x image_.
5. In the second **<article>** , add a **<picture>**. It should have child elements of:

- **<source>** with a **media** attribute set to a **"(min-width:1024px)"** and a **srcset** of
       **"kitten-large.png"** ;
- **<source>** with a **media** attribute set to a **"(min-width: 667px)"** and a **srcset** of
       " **kitten-medium.png"** ;
- **<img>** with a **src** of **"kitten-small.png"** and **alt** of **"Cute Kitten"**.

6. Save the file and view in the browser. Changing the width of the device through the
    _Device Selector_ being set to _Responsive_ should change the image as the width is
    increased or decreased.
7. In the third **<article>** , add an **<img>** with attributes set to:

- **src** of **"small.jpg"** ;
- **alt** of **"Cute Kitten"** ;
- **sizes** set to **"50vw"** ;
- **srcset** of **"kitten-small.png 500w, kitten-medium.png 1000w, kitten-large.png**
       **1500w"**.

8. Save the file and change the Responsive width of the Device Selector to be around
    40 0 pixels.
9. Refresh the page and note that the **kitten-small.png** image is shown.
10. Increase the width of the available screen and note that the image changes to
    the larger ones as breakpoints are hit.
11. Once the **kitten-large.png** image is shown, _refresh_ the page again.
12. Decrease the width of the available screen and note that the image _DOES NOT_
    change.

> This is the end of Quick Lab 14
