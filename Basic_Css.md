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
