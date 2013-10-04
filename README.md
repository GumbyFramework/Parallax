Gumby Parallax Module
=====================

This UI module applies a simple background image parallaxing effect. For more detailed documentation please check out the [Gumby docs](http://gumbyframework.com).

Installation
------------

A bower package is available to install this repo into your project. We recommend using this method to install Gumby and any extra UI modules, however you can alternatively move the individuals files into your project.

	$ bower install gumby-parallax

Include gumby.parallax.js in the same fashion as your other UI modules, after gumby.js and before gumby.init.js. In production you should minify JavaScript files into a single optimized gumby.min.js file, ensuring the order (gumby.js, UI modules, gumby.init.js) is retained. 

	<!--
	Include gumby.js followed by UI modules.
	Or concatenate and minify into a single file-->
	<script src="js/libs/gumby.js"></script>
	<script src="js/libs/ui/gumby.skiplink.js"></script>
	<script src="js/libs/ui/gumby.toggleswitch.js"></script>
	<!-- included from Bower's components directory -->
	<script src="components/gumby-parallax/gumby.parallax.js"></script>
	<script src="js/libs/gumby.init.js"></script>
	
	<!-- In production minifiy and combine the above files into gumby.min.js -->
	<script src="js/libs/gumby.min.js"></script>
	<script src="js/plugins.js"></script>
	<script src="js/main.js"></script>
	
Import the _parallax.scss partial in the same fashion as your other imports. Once you compile sass you are good to go.

	// imported from Bower's components directory
	@import "../components/parallax";


Usage
-----

Using the parallax module is simple. Add a class of `parallax` to the element ensuring it has a fixed height and a background image. Use the `gumby-parallax` attribute to specify the ratio at which the background image moves relative to the users scroll. The window scroll event will be used unless another element is specified in `gumby-holder`. The bg image will reach 0px Y position when the element itself reaches the top of the window, you can specify a px value in `gumby-offset` with which to offset this 'end point'.

	<!-- bg position will scroll at half the speed of windows natural scroll -->
	<!-- bg will be positioned at 0 0 when element is 100px from top of window -->
	<div class="parallax" gumby-parallax="0.5" gumby-offset="100"></div>

If you have a large and complex DOM, the position of the element may depend on the window being fully loaded. In this case we recommend manually initializing Parallax after window load.


**MIT Open Source License**

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

	
	
