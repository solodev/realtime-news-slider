# realtime-news-slider
A reoccurring problem is how to maximize space within these modules/widgets while still presenting your users a plethora of options. One method to solve this problem is your turn your recent news module into a realtime slider. This allows users to see a number of news entries within a confined area.

Using [Slick Slider](http://kenwheeler.github.io/slick/), we can add slider capabilities to a standard news module so your users can easily browse your most recent content.

## Tutorial

For detailed instructions, view Solodev's [Adding a Realtime News Slider to Your Web Design Project](https://www.solodev.com/blog/web-design/sliders/adding-a-realtime-news-slider-to-your-web-design-project.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/36o96dm2/).

## HTML

The news slider contains the following basic HTML markup:
```
<div class="container">
  <div class="row">
    <div class="col-md-6 news-slider">
  
	<div class="slide">
	  <div class="blogPost--small">
		<div class="media">
		  <span class="pull-left"><a href="#"><span class="date"><span>29</span> <small>Mar</small></span></a></span>
		  <div class="media-body">
			<h4 class="media-heading">
			  <a href="#">Building In WebCorpCo CMS 8</a>
			</h4>
			<p>
			  Learn about all of the possibilities of web design in our latest CMS release.
			</p>
		  </div>
		</div>
	  </div><!-- / blogPost -->
	  <div class="blogPost--small">
		<div class="media">
		  <span class="pull-left"><a href="#"><span class="date"><span>22</span> <small>Mar</small></span></a></span>
		  <div class="media-body">
			<h4 class="media-heading">
			  <a href="#">WebCorpCo Named To Inc. 5000</a>
			</h4>
			<p>
			  Inc. magazine today ranked WebCorpCo as the 1,870th fastest growing company on the 34th annual Inc. 5000.
			</p>
		  </div>
		</div>
	  </div><!-- / blogPost -->
	</div><!-- / slide1 -->
	
	<div class="slide">
	  <div class="blogPost--small">
		<div class="media">
		  <span class="pull-left"><a href="#"><span class="date"><span>12</span> <small>Mar</small></span></a></span>
		  <div class="media-body">
			<h4 class="media-heading">
			  <a href="#">7 Critical Factors When Choosing A CMS</a>
			</h4>
			<p>
			  Finding a solution that can be tailored to support the needs of your business is more important than ever.
			</p>
		  </div>
		</div>
	  </div><!-- / blogPost -->
	  <div class="blogPost--small">
		<div class="media">
		  <span class="pull-left"><a href="#"><span class="date"><span>10</span> <small>Mar</small></span></a></span>
		  <div class="media-body">
			<h4 class="media-heading">
			  <a href="#">What Is A Content Management System</a>
			</h4>
			<p>
			  So many acronyms that most of us know a brief amount about, if at all, let alone the meaning of those three little letters we hear so often.
			</p>
		  </div>
		</div>
	  </div><!-- / blogPost -->
	</div><!-- / slide2 -->

    </div>
  </div>	
</div>

<div class="container newsNav">
	<div class="row">
		<div class="col-md-3">
			<a href="#" class="link-underline">See All News</a>
		</div>
		<div class="col-md-3 text-right">
			<button id="ct-js-district-calendar--prev" type="button" class="slick-arrow next"><img src="https://www.solodev.com/assets/news-slider/arrow-prev.jpg" alt="Previous"></button>
			<button id="ct-js-district-calendar--next" type="button" class="slick-arrow next"><img src="https://www.solodev.com/assets/news-slider/arrow-next.jpg" alt="Next"></button>
		</div>
	</div>
										
</div>
```
## CSS

All required CSS can be found in news-slider.css

## JS

All needed JS is below and in news-slider.js:
```
$(document).ready(function(){
			$('.news-slider').slick({
				slidesToShow: 1,
				slidesToScroll: 1,
				autoplay: true,
				autoplaySpeed: 8000,
				arrows: true,
        prevArrow: $('.prev'),
        nextArrow: $('.next'),
				dots: false,
					pauseOnHover: false,
					responsive: [{
					breakpoint: 768,
					settings: {
						slidesToShow: 1
					}
				}, {
					breakpoint: 520,
					settings: {
						slidesToShow: 1
					}
				}]
			});
		});
```

## External Includes

This tutorial contains the following third party resources.

```
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
<link href="news-slider.css" rel="stylesheet">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.6.0/slick.js"></script>
<script src="news-slider.js"></script>
```

