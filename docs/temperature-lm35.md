<!--remove-start-->

# Temperature - LM35

<!--remove-end-->






##### Breadboard for "Temperature - LM35"



![docs/breadboard/temperature-lm35.png](breadboard/temperature-lm35.png)<br>

Fritzing diagram: [docs/breadboard/temperature-lm35.fzz](breadboard/temperature-lm35.fzz)

&nbsp;




Run with:
```bash
node eg/temperature-lm35.js
```


```javascript
var five = require("johnny-five");

five.Board().on("ready", function() {
  var temperature = new five.Temperature({
    controller: "LM35",
    pin: "A0"
  });

  temperature.on("data", function() {
    console.log(this.celsius + "°C", this.fahrenheit + "°F");
  });
});


```








## Additional Notes
- [LM35 - Temperature Sensor](http://www.ti.com/product/lm35)

&nbsp;

<!--remove-start-->

## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.

<!--remove-end-->
