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

