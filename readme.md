# Jekyll + Foundation SCSS #

Foundation self declares to be the most advanced responsive front-end framework in the world.

## What's Included: ##
* all the directories that Jekyll needs to compile your static site
* jQuery
* the entire foundation framework
* a default html5 template in _layouts
* a default nav bar under _includes
* default index and 404 page, along with 3 other empty pages


## How To 'Install' It ##

First, make sure you have [Ruby](https://www.ruby-lang.org/en/) and the [Jekyll](http://jekyllrb.com/) gem installed (```gem install jekyll```).

Then, just download the .zip or

	git clone git@github.com:rememberlenny/Jekyll-Foundation-SASS.git

## How To 'Run' It ##

**Serving Jekyll**
To set up a local development server use the command ```jekyll serve```. The files from ```_site``` will be served to [http://localhost:4000](http://localhost:4000) by default.

**SASS -> CSS**
To compile the SASS files into CSS, run ```compass watch```. Files from ```sass/*``` will render to ```_source/assets/css```.

**Preparing for build**
After you have compiled your SASS with Compass, its time build. Build for deploymentwith the command ```jekyll build```. The files will render to ```_site```.


## Tutorial: ##

### Layouts ###

The easiest way is to use the default layout (HTML5 Boilerplate -- _layouts/default.html). To use a layout, put this at the top of your page:

    ---
    layout: default
    title: YourPageTitleHere
    ---

<h1>Page-Specific HTML Content</h1>
<p>etc...</p>



### Includes ###

If you're planning on reusing a few snippets of code on several pages, DRY (Don't Repeat Yourself)! Create an include HTML file and put it in the _includes/ directory. Kind of like a Rails helper.

To call an include in a page, just write

    {% include yourincludename.html %}


For an example of this, see _layouts/default.html -- I include the nav.html snippet on the default layout, meaning it displays on every page that uses that layout.


### Slideshows ###

Foundation's Orbit code is ready to plug into your website; the javascript to trigger it can be found in _includes/orbit.html -- just include that on the page where you want a slideshow, and then add a div#slideshow with image tags inside:

    <div id="slideshow">
    	<img src="something.jpg" alt="blah">
    	<img src="somethingelse.jpg" alt="yeah">
    	<img src="foo.jpg" alt="bar">
    </div>

For more information see [Zurb's Foundation documentation.](http://foundation.zurb.com/docs/orbit.php)



## That's It! ##

Have Fun and make some cool websites.

Comments, improvements, and suitcases filled with money can be sent to lenny@atriangle.com


-Lenny

## Thanks ##

Thanks to [Dave Cohen](https://github.com/groovemonkey) for making [jekyll-foundation-base](https://github.com/groovemonkey/jekyll-foundation-base):.