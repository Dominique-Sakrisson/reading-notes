# Chart.js Api article

The article covered the setup of chart js into a project. First the project needs a reference to the chart library, 
which we can either use a cdn in the header of our file or download the files from chart js and include in our project directory..
There were 3 charts demonstrated in the article, line chart, pie chart and a bar chart. 
The chart lives in a html canvas tag. For which we need the refernce to and then call new Chart. The chart will populate to he page when 
the function to create the chart is called with proper data and other properties
```
// line chart data
            var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);

```


# Basic usage of canvas
This as the title states instructs on basic usage for the canvas tag. The tag like any others can have different attributes, `height,width,id` 
Sometimes like images the canvas will not be supported by the users browser. In which case intead of using an alt tag we can type our alternative rendering directly between the 
    `<canvas>   here will render as normal text if canvas is not supported</canvas>`
In order for the canvas to populate anything to the screen we have to use a special function in our js.
Since its always a good idea to test for thing first, to do with canvas its convention to test for the canvas node's `getContext`
```
var canvas = document.getElementById('tutorial');

if (canvas.getContext) {
  var ctx = canvas.getContext('2d');
  // drawing code here
} else {
  // canvas-unsupported code here
}
```

heres an example of the canvas in action
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8"/>
  <script type="application/javascript">
    function draw() {
      var canvas = document.getElementById('canvas');
      if (canvas.getContext) {
        var ctx = canvas.getContext('2d');

        ctx.fillStyle = 'rgb(200, 0, 0)';
        ctx.fillRect(10, 10, 50, 50);

        ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';
        ctx.fillRect(30, 30, 50, 50);
      }
    }
  </script>
 </head>
 <body onload="draw();">
   <canvas id="canvas" width="150" height="150"></canvas>
 </body>
</html>
```
