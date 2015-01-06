### Rails Asset Pipeline Clinic

**Assets:** JavaScript, CSS, and other static files we need to properly render
our pages.

Solves:
*  Allows you to nest JS and CSS files in subdirectories
*  No longer need to specify the exact order to include files for third party
   libraries like Bootstrap or Foundation
*  Compresses all our assets so they get served to the browser faster
*  Consolidate CSS and JS files into one file so there are less HTTP requests
   made by the browser, improving page load speed.
*  Allow us to use preprocessors like Sass or Coffee Script. 
*  Enables caching to further increase page speeds and will re cache assets when
   changes are made.


#### Three Places To Store Assets:

app/assets - file specific to current project
lib/assets - files for internal libraries
vendor/assets - files for external libraries

#### Manifest Files

app/assets/javascripts/application.js
app/assets/stylesheets/application.css

The manifest files specify where to find other files to load in and in which
order to load them.

In order to add to manifest you need there to be a comment in the beginning of
the line and an equals sign.

```javascript
//= require foo   # single line comment

/*
 * 
 *
 *= require foo    # multi line comment
*/
```


