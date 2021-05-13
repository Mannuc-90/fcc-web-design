## <center>Basic CSS</center>
### Adding styles:
1.  ***Inline Styles***: using style declaration within an element.
    ```css
    <h2 style="color: blue;">CatPhotoApp</h2>
    ```
    
2.  Using style in the header section:
    ```css
    <style>
    h2{
        color:blue;
    }
    </style>
    ```

3. Linking an external css file:
    ```css
    <link rel="stylesheet" href="style.css">
    ```

#### CSS Properties:

-   ***color*** : To change color of text
    ```css
    h2 {
            color: red;
        }
    ```
    
-   ***class*** : reusable styles that can be added to HTML elements. Classes allow you to use the same CSS styles on multiple HTML elements
    ```css
    <style>
    .blue-text {
        color: blue;
    }
    </style>
    <main>
    <h2 class="blue-text">CatPhotoApp</h2>
    </main>
    ```

-   ***font-size***: Change the Font Size of an Element
    ```css
    h1 {
        font-size: 30px;
    }
    ```

-   ***font-family*** : Change th efont-family
    ```css
    h2 {
        font-family: sans-serif; /* monospace */
    }
    ```
 -  ***Import a Google Font***:To use Google Fonts copy the font's URL from the Google Fonts library and then paste it in your HTML
    ```css
    <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
    ```
    Now you can use the Lobster font in your CSS by using Lobster as the FAMILY_NAME
    ```css
    font-family: FAMILY_NAME, GENERIC_NAME;
    ```
    The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.

    Family names are case-sensitive and need to be wrapped in quotes if there is a space in the name. For example, you need quotes to use the "Open Sans" font, but not to use the Lobster font.
    eg
    ```css
    h2{
        font-family: Lobster;
    }
    ```

    ***Specify How Fonts Should DegradePassed*** : There are several default fonts that are available in all browsers. These generic font families include monospace, serif and sans-serif

    When one font isn't available, you can tell the browser to "degrade" to another font.

    Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.
    
    eg
    ```css
    p {
        font-family: Helvetica, sans-serif;
    }
    ```
-   ***width***: controls an element's width
    ```css
    <style>
    .larger-image {
        width: 500px;
    }
    </style>
    ```

-   ***border***: Add Borders Around Your Elements. CSS borders have properties like style, color and width.    
    ```css
    <style>
    .thin-red-border {
        border-color: red;
        border-width: 5px;
        border-style: solid;
    }
    </style>
    ```
 
-   ***border-radius***: Add Rounded Corners with border-radius
    ```css
    <style>
    .thin-red-border {
        border-radius:10px;
    }
    </style>
    ```
    In addition to pixels, you can also specify the border-radius using a percentage.

    border-radius of 50% Make Circular Images
    ```css
    .thick-green-border {
        border-color: green;
        border-width: 10px;
        border-style: solid;
        border-radius: 10px;
        border-radius:50%;
    }
    ```

-   ***background-color*** : You can set an element's background color with the background-color property.
    ```css
    .green-background {
    background-color: green;
    }
    ```

-   ***id***: In addition to classes, each HTML element can also have an id attribute.

    There are several benefits to using id attributes: You can use an id to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

    id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice
    ```css
    <h2 id="cat-photo-element">
    ```
    an id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied.
    ```css
    #cat-photo-element {
    background-color: green;
    }
    ```

-   ***padding, border, and margin***:

    Three important properties control the space that surrounds each HTML element: padding, border, and margin.

-   ***padding*** : An element's padding controls the amount of space between the element's content and its border.
    ```css
    <style>
    .injected-text {
        margin-bottom: -25px;
        text-align: center;
    }

    .box {
        border-style: solid;
        border-color: black;
        border-width: 5px;
        text-align: center;
    }

    .yellow-box {
        background-color: yellow;
        padding: 10px;
    }

    .red-box {
        background-color: crimson;
        color: #fff;
        padding: 20px;
    }

    .blue-box {
        background-color: blue;
        color: #fff;
        padding: 10px;
    }
    </style>
    <h5 class="injected-text">margin</h5>

    <div class="box yellow-box">
    <h5 class="box red-box">padding</h5>
    <h5 class="box blue-box">padding</h5>
    </div>
    ```
    ***Add Different Padding to Each Side of an ElementPassed***:

    Sometimes you will want to customize an element so that it has different amounts of padding on each of its sides.

    CSS allows you to control the padding of all four individual sides of an element with the padding-top, padding-right, padding-bottom, and padding-left properties.
    ```css
    .red-box {
        background-color: crimson;
        color: #fff;
        padding-top: 40px;
        padding-right: 20px;
        padding-bottom: 20px;
        padding-left: 40px;
    }
    ```

    ***Use Clockwise Notation to Specify the Padding of an Element***:

    Instead of specifying an element's padding-top, padding-right, padding-bottom, and padding-left properties individually, you can specify them all in one line, like this:
    ```css
    padding: 10px 20px 10px 20px;
    ```

    These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific padding instructions.


-   ***margin*** : An element's margin controls the amount of space between an element's border and surrounding elements.

    When you increase the blue box's margin, it will increase the distance between its border and surrounding elements
    ```html
    <style>
    .injected-text {
        margin-bottom: -25px;
        text-align: center;
    }

    .box {
        border-style: solid;
        border-color: black;
        border-width: 5px;
        text-align: center;
    }

    .yellow-box {
        background-color: yellow;
        padding: 10px;
    }

    .red-box {
        background-color: crimson;
        color: #fff;
        padding: 20px;
        margin: 20px;
    }

    .blue-box {
        background-color: blue;
        color: #fff;
        padding: 20px;
        margin: 10px;
    }
    </style>
    <h5 class="injected-text">margin</h5>

    <div class="box yellow-box">
    <h5 class="box red-box">padding</h5>
    <h5 class="box blue-box">padding</h5>
    </div>
    ```
    ***Add a Negative Margin to an Element***: If you set an element's margin to a negative value, the element will grow larger.

    ***Add Different Margins to Each Side of an Element*** : 

    Sometimes you will want to customize an element so that it has a different margin on each of its sides.

    CSS allows you to control the margin of all four individual sides of an element with the margin-top, margin-right, margin-bottom, and margin-left properties.
    ```css
    .red-box {
        background-color: crimson;
        color: #fff;
        margin-top: 40px;
        margin-right: 20px;
        margin-bottom: 20px;
        margin-left: 40px;
    }
    ```

    ***Use Clockwise Notation to Specify the Margin of an Element***: 

    Instead of specifying an element's margin-top, margin-right, margin-bottom, and margin-left properties individually, you can specify them all in one line, like this:
    ```css
    margin: 10px 20px 10px 20px;
    ```

    These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific margin instructions.

-  ***Use Attribute Selectors to Style Elements*** : 
There are CSS Selectors you can use to select custom groups of elements to style.
```css
    <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
    <style>
    .red-text {
        color: red;
    }

    h2 {
        font-family: Lobster, monospace;
    }

    p {
        font-size: 16px;
        font-family: monospace;
    }

    .thick-green-border {
        border-color: green;
        border-width: 10px;
        border-style: solid;
        border-radius: 50%;
    }

    .smaller-image {
        width: 100px;
    }

    .silver-background {
        background-color: silver;
    }
    </style>

   
    <main>
    <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>

    <a href="#"><img class="smaller-image thick-green-border" src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

    <div class="silver-background">
        <p>Things cats love:</p>
        <ul>
        <li>cat nip</li>
        <li>laser pointers</li>
        <li>lasagna</li>
        </ul>
        <p>Top 3 things cats hate:</p>
        <ol>
        <li>flea treatment</li>
        <li>thunder</li>
        <li>other cats</li>
        </ol>
    </div>

    <form action="https://freecatphotoapp.com/submit-cat-photo" id="cat-photo-form">
        <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
        <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
        <label><input type="checkbox" name="personality" checked> Loving</label>
        <label><input type="checkbox" name="personality"> Lazy</label>
        <label><input type="checkbox" name="personality"> Energetic</label><br>
        <input type="text" placeholder="cat photo URL" required>
        <button type="submit">Submit</button>
    </form>
    </main>
```
use the [attr=value] attribute selector to style the checkboxes in CatPhotoApp. This selector matches and styles elements with a specific attribute value. 
    
For example, the below code changes the margins of all elements with the attribute type and a corresponding value of radio:

```css
    [type='radio'] {
    margin: 20px 0px 20px 0px;
    }
```

***Understand Absolute versus Relative Units*** : 

The two main types of length units are absolute and relative

-   Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively
-   Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.
    ```css
    .red-box {
        background-color: red;
        margin: 20px 40px 20px 40px;
        padding:1.5em;

    }
    ```
***Style the HTML Body Element***

```css
body {
     background-color: black;
 }
```
Example:
```css
<style>
  body {
    background-color: black;
    color:green;
    font-family :monospace;
  }

</style>

<body>
    <h1>Hello World</h1>
</body>
```

***Styles Overriding Rules***
-   For multiple classes on same element, the order of class declarations in style matters. he later style overrides the earlier style
-   If there is 1 class and 1 id on same element, id takes precedence
-   Inline styles take more importance than class or id
-   Override All Other Styles by using Important:
    
    In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important.
    ```css
    color: red !important;
    ```

***Use CSS Variables to change several elements at once***
```css
Create Custome variable
--penguin-skin: black;

Use custom variable:
background: var(--penguin-skin);

```

<u>Penguin</u>
```css
<style>
  .penguin {

    /* Only change code below this line */
    --penguin-skin: black;
    --penguin-belly: gray;
    --penguin-beak: yellow;
    /* Only change code above this line */

    position: relative;
    margin: auto;
    display: block;
    margin-top: 5%;
    width: 300px;
    height: 300px;
  }

  .penguin-top {
    top: 10%;
    left: 25%;
    background: var(--penguin-skin, gray);
    width: 50%;
    height: 45%;
    border-radius: 70% 70% 60% 60%;
  }

  .penguin-bottom {
    top: 40%;
    left: 23.5%;
    background: var(--penguin-skin, gray);
    width: 53%;
    height: 45%;
    border-radius: 70% 70% 100% 100%;
  }

  .right-hand {
    top: 0%;
    left: -5%;
    background: var(--penguin-skin, gray);
    width: 30%;
    height: 60%;
    border-radius: 30% 30% 120% 30%;
    transform: rotate(45deg);
    z-index: -1;
  }

  .left-hand {
    top: 0%;
    left: 75%;
    background: var(--penguin-skin, gray);
    width: 30%;
    height: 60%;
    border-radius: 30% 30% 30% 120%;
    transform: rotate(-45deg);
    z-index: -1;
  }

  .right-cheek {
    top: 15%;
    left: 35%;
    background: var(--penguin-belly, white);
    width: 60%;
    height: 70%;
    border-radius: 70% 70% 60% 60%;
  }

  .left-cheek {
    top: 15%;
    left: 5%;
    background: var(--penguin-belly, white);
    width: 60%;
    height: 70%;
    border-radius: 70% 70% 60% 60%;
  }

  .belly {
    top: 60%;
    left: 2.5%;
    background: var(--penguin-belly, white);
    width: 95%;
    height: 100%;
    border-radius: 120% 120% 100% 100%;
  }

  .right-feet {
    top: 85%;
    left: 60%;
    background: var(--penguin-beak, orange);
    width: 15%;
    height: 30%;
    border-radius: 50% 50% 50% 50%;
    transform: rotate(-80deg);
    z-index: -2222;
  }

  .left-feet {
    top: 85%;
    left: 25%;
    background: var(--penguin-beak, orange);
    width: 15%;
    height: 30%;
    border-radius: 50% 50% 50% 50%;
    transform: rotate(80deg);
    z-index: -2222;
  }

  .right-eye {
    top: 45%;
    left: 60%;
    background: black;
    width: 15%;
    height: 17%;
    border-radius: 50%;
  }

  .left-eye {
    top: 45%;
    left: 25%;
    background: black;
    width: 15%;
    height: 17%;
    border-radius: 50%;
  }

  .sparkle {
    top: 25%;
    left: 15%;
    background: white;
    width: 35%;
    height: 35%;
    border-radius: 50%;
  }

  .blush-right {
    top: 65%;
    left: 15%;
    background: pink;
    width: 15%;
    height: 10%;
    border-radius: 50%;
  }

  .blush-left {
    top: 65%;
    left: 70%;
    background: pink;
    width: 15%;
    height: 10%;
    border-radius: 50%;
  }

  .beak-top {
    top: 60%;
    left: 40%;
    background: var(--penguin-beak, orange);
    width: 20%;
    height: 10%;
    border-radius: 50%;
  }

  .beak-bottom {
    top: 65%;
    left: 42%;
    background: var(--penguin-beak, orange);
    width: 16%;
    height: 10%;
    border-radius: 50%;
  }

  body {
    background:#c6faf1;
  }

  .penguin * {
    position: absolute;
  }
</style>
<div class="penguin">
  <div class="penguin-bottom">
    <div class="right-hand"></div>
    <div class="left-hand"></div>
    <div class="right-feet"></div>
    <div class="left-feet"></div>
  </div>
  <div class="penguin-top">
    <div class="right-cheek"></div>
    <div class="left-cheek"></div>
    <div class="belly"></div>
    <div class="right-eye">
      <div class="sparkle"></div>
    </div>
    <div class="left-eye">
      <div class="sparkle"></div>
    </div>
    <div class="blush-right"></div>
    <div class="blush-left"></div>
    <div class="beak-top"></div>
    <div class="beak-bottom"></div>
  </div>
</div>
```

***Attach a Fallback value to a CSS Variable***
When using your variable as a CSS property value, you can attach a fallback value that your browser will revert to if the given variable is invalid.

Note: This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.
```css
background: var(--penguin-skin, black);
```
This will set background to black if your variable wasn't set. Note that this can be useful for debugging.

***Inherit CSS Variables***
When you create a variable, it is available for you to use inside the selector in which you create it. It also is available in any of that selector's descendants. This happens because CSS variables are inherited, just like ordinary properties.

To make use of inheritance, CSS variables are often defined in the :root element.

:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet