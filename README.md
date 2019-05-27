# ScrollDetection.js

Copyright (c) 2019 [Chris Campbell](https://github.com/christophertcampbell); License: MIT

## About

Lightweight Javascript package for detecting browser scroll amount and applying pixel/percent-based css classes to the &lt;body> element.  Useful for targeted css styling based on browser scroll amount.

* Pixel and percent-based css classes can be applied on an incrementing basis up to configurable limits.
	* Ex: `.scrolled-1`, `.scrolled-2`, `.scrolled-3` ... (Pixels)
	* Ex: `.scrolled-pct-1`, `.scrolled-pct-2`, `.scrolled-pct-3` ... (Percent)

* Pixel and percent-based css classes can be applied and remain at configurable "sticky" distances
	* Ex: `.scrolled-100`, `.scrolled-200`, `.scrolled-300` ... (Pixels)
	* Ex: `.scrolled-pct-5`, `.scrolled-pct-10`, `.scrolled-pct-20` ... (Percent)

## How to Use

### 1. Include the ScrollDetection.js distributable in your project

`scroll-detection.js` can be found in the `/src/` directory of this repository.

```javascript
<script type="text/javascript" src="path/scroll-detection.js"></script>
```

### 2. Change the default configuration (optional)

```javascript
var config = window.ScrollDetection.getConfig();

/* Default config object returned by above:
{
	pixel: {
		singleClassesUntil: 200,
		stickyDistances: [50, 100, 150, 200, 300]
	},
	percent: {
		singleClassesUntil: 100,
		stickyDistances: [25, 50, 75]
	}
}
*/

// Change the configuration
config.percent.stickyDistances = [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]; // Our new distances
window.ScrollDetection.setConfig(config);
```

## License

ScrollDetection.js is licensed under the MIT license (http://opensource.org/licenses/MIT)

## GitHub Repo

https://github.com/christophertcampbell/scroll-detection.js