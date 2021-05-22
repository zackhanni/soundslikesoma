# Sounds Like Soma 2.0
 

![Site Logo](https://github.com/zackhanni/zackhanni.github.io/blob/master/img/intro-header.jpg)

Sounds Like Soma was founded by acclaimed producer, mixing and mastering engineer Zack Hanni in 2007. He developed the studio to have a relaxed, laid-back atmosphere, with the commitment, equipment, and quality of a major recording studio. 

His competitive rates and ability to exceed expectations have kept clients coming back, time and time again. 

Come in and record a song with us to find out for yourself why were voted one of the best recording studios in Philadelphia.


- - -

# TO DO

add new youtube videos to a new page for video tutorials and lessons

set up mailchimp for people to sign up and hear about new music releases each month or big events happening , discounts, and more!

remove team tab? at least from top bar. many only accecable from homepage.

Add pictures to testimonials. show them live at work doing something in studio. reference rec.

more information on homepage services

remove payment options. people usually ask to confirm anyway.

Book with Gage or Zack instead of studio A or B to make it less confusing?

schedule a tour button on top bar? gets their email and sets up a time to talk.

about page - 'our story' telling people about who we are and what were about. Maybe also have the "why choose soma" part here.

get emily to draw cleaner 'features' images
make feature images 100x100px

get testimonials from bigger / more important artists (like tye, limm, etc.)

add video testimonials to the testimonials page

add studio images on homepage. maybe instagram too

better logo instead of "soma" in the top corner

add mailchimp signup at bottom

add meta information to pages

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



