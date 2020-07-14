# Attractive Data | Using Chart.js and Canvas 

![stunning](https://media.giphy.com/media/iBjbPrCiuOeIIBqESG/giphy.gif)

#### Heads will turn after Chart.js and Canvas display your data in an elegant fashion. Let's learn!

* We're all familiar with charts and graphs and understand that they can display data in a single view
* Charts.js takes it up a level by displaying animated charts 
* It is a JavaScript [plugin](https://www.computerhope.com/jargon/p/plugin.htm) that uses HTML5's canvas element to draw graphs

### So, how do we use Chart.js? Here's a helpful and easy guide to get you started:

1. Download [Chart.js](https://www.chartjs.org/)
1. Next, create a canvas element in your HTML by adding this to your HTML doc:
```
<canvas id="buyers" width="600" height="400"></canvas>
```
3. A script needs to be written that will retrieve the context of the canvas so add this to the bottom of your HTML body:
```
<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```
4. Next, you'll need some data to work with! Any data you have will be inserted into the same  `<script></script>` tag
5. Test your data inside your browser. YAY! You did it!

-------------------
### Now that you know how cool Chart.js is, I know you'll be excited to learn more about the `<canvas>` element
![excited](https://media.giphy.com/media/rkxgklAlMgLwA/giphy.gif)

### Earlier we talked about how Chart.js and Canvas work together to transform your data. Well, you need to know a bit more about what this element does and what its capabilities are:

1. Canvas is used to draw graphics quickly using JavaScript
2. Canvas does look quite similar to the `<img> ` element but it **DOES NOT** include an `src` or `alt` attribute
3. The canvas element only has **TWO** attributes and those are `width` and `height`
4. The canvas element can be styled like other images but styles rules **WILL NOT** alter the acutal drawing
5. When using this element, don't forget to provide [FALLBACK CONTENT](https://www.w3.org/html/wg/wiki/DefinitionFallBackContent) just in case something goes wrong
6. The `<canvas>` tag does require it's closing tag `</canvas>`
7. A script will need to access the [rendering context](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D) to draw on it
8. The method `getContext()` is used to get the rendering context and its drawing functions
9. Before the `getContext` element can be used, the script needs to retrieve the node in the DOM that represents the canvas element (use `getDocumentById()`)
10. Now that you have the element node, you can use `getContext'

### Now that you know how Chart.js and canvas work together, go out there and draw some [shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)!
