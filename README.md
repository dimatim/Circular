# Circular
Simple way of creating indeterminate circular loading indicators; all you need is a canvas. Uses jQuery.<br>
Check out the <a href="https://youtu.be/rdgqdj_l2aQ">demo</a>


#Usage
```js
var config = {
        canvas: $('#someCanvasId'),   //canvas element
        colors: [                     //colors and start offsets in radians (each color entry will result in a circle)
            {color: '#FFD034', offset: 0},
            {color: '#0072BB', offset: Math.PI / 4},
            {color: '#FF4C3B', offset: Math.PI / 2},
            {color: '#666699', offset: 3 * Math.PI / 4},
            {color: '#003366', offset: Math.PI}
        ],
        duration: 2000,               //animation cycle duration in miliseconds
        reverse: false,               //reverse direction; by default is clockwise
        repeat: 3,                    //repeats the defined colors N times
        spacing: 6,                   //spacing between circles in pixels
        lineWidth: 3,                 //line width in pixels
        maxRadius: 50,                //maximum radius of the loading indicator
        minRadians: Math.PI / 3,      //smallest arc in radians
        maxRadians: 6 / 4 * Math.PI   //biggest arc in radians
    };
    startSpinner(config);             //starts the animation
    ...
    stopSpinner('someCanvasId');      //stops the animation for the specified canvasId
```
#Dependencies
jQuery
