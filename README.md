# Sounds Like Soma 2.0
 

![Site Logo](https://github.com/zackhanni/zackhanni.github.io/blob/master/img/intro-header.jpg)

- - -

# TO DO

set up mailchimp for people to sign up and hear about new music releases each month or big events happening , discounts, and more!



reference abbey roads stuido
	- make services page descriptions consice.
	- mail signup at bottom
	- covid page at bottom
	- FAQ page at bottom
	- partners page (make wonders etc?_3)
	- social medip pages at bottom
	gear list down there and not in menu
	- page on what we are doing about covid safty
	- up to 3 people, 


- - -

# --- Resources ---

blog posts dont show up ( similar to services)
solution - needed to run bundle update (still have no idea why this needed to happen before they could show up)



# HOW TO CHANGE PICS n THINGS

svg images in _sass > pages > services, team, testimonials, etc.

## page images
_sass > pages > home.scss
_sass > pages > services, team, testimonials > _page-NAME-list.scss

## homepage 'why choose soma' pics
_data > features.json

## home headers (our services, why choose soma)
index.html > manual changeing to light or dark etc

## p tags for under headers
_scss > components > _intro > line 42

## navbar color
_scss > components > _header > line 4 background color

## testimonial title color
_scss > pages > testimonials > testimonials-summary > line 32

## HOW TO CHANGE BG/FONT COLOR

## all pages main background color and text
_sass > bootstrap > variables > line 143-144

## change small window on home page
_sass > pages > _home.scss > .call 

## homepage feature background color
_sass >  components > _feature 

- - -

## colors and theme info
https://getbootstrap.com/docs/4.0/getting-started/theming/


cd into Documents/Github/Project
bundle exec jekyll serve



