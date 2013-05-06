SVG CSS Image Fallback
======================
###A cross-browser compatible method of implementing background-image SVGs in your SCSS

###### V1.1

---

A [Compass](http://compass-style.org) mixin for simply using resolution-independant SVG files in your sites.

[Original technique written by Pau Giner](http://pauginer.tumblr.com/post/36614680636/invisible-gradient-technique).

# 


###### Get the repo from github

	git pull git@github.com:MarnuLombard/SVG-CSS-Image-Fallback.git
		
###### Import the mixin into your scss
	@import "mixins/svg-fallback";
	
---

### To use:
###### Call the mixin and reference your image
	@include svg-fallback("your-image", position-y, position-x, repeat);
*Remember to have both a png and an svg by the same name in your images folder*

###### This will output
	background-image: url('../img/your-image.png');
	background-image: -webkit-linear-gradient(left, transparent, transparent), url('../img/your-image.svg');
	background-image: -moz-linear-gradient(left, transparent, transparent), url('../img/your-image.svg');
	background-image: -o-linear-gradient(left, transparent, transparent), url('../img/your-image.svg');
	background-image: linear-gradient(left, transparent, transparent), url('../img/your-image.svg');
	background-position: center center;
	background-repeat: no-repeat;
*position-y, position-x and repeat have defaults, so you can leave them out*


	