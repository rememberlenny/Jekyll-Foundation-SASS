# Jekyll + Foundation CSS #

I love Zurb's Foundation framework, and Jekyll is a great tool for preventing code duplication while building static HTML/CSS/js websites.

This tool really just exists to create a "base" directory for starting new projects.

## What's Included: ##
* all the directories that Jekyll needs to compile your static site
* jQuery
* a stripped-down version of the foundation framework -- just the grid and orbit slideshow.
* a default html5 template in _layouts
* a default nav bar under _includes
* orbit slideshow js code in _includes, ready to be called on any page
* default index and 404 page, along with 3 other empty pages


## How To 'Install' It ##

First, make sure you have Ruby and the Jekyll gem installed (gem install jekyll).

Then, just download the .zip or

	```git clone git://github.com/groovemonkey/jekyll-foundation-base.git```

this baby and get started! Because now other people are using this now, I wrote a small tutorial (below).

I hope you find this useful; it has certainly made me more productive.

Cheers!



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

That's it.


## Known Issues ##

I haven't thought of a clever way to get jekyll or moustache to automatically apply page-specific HTML IDs to elements, e.g.

"""
menu.each do |menu_item| 
	if menu_item.src == current_page_url
		menu_item.id = "active"
	end
end
"""

I recommend doing this in a Javascript include that you place in the default template, but that will degrade the experience for people who don't let JS execute in their browsers (although those people will probably be used to a degraded web browsing experience...).




## That's It! ##

Have Fun and make some cool websites.

Comments, improvements, and suitcases filled with money can be sent to dave@dave-o-matic.com


-Dave