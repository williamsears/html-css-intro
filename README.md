# HTML + CSS Workshop!

## Base instructions
* Fork this repo, and clone your fork into a new Cloud9 workspace.
* Specifically for this workshop, **each exercise's branch should be branched off the previous exercise**. You will make
one pull request per exercise as usual, but instead of branching off master, you'll be building up your work branch
after branch.

## Exercise 1: moving out
* For this exercise, you will stay in the **master branch**. In this exercise, you are going to move the CSS that
we put inside of the `<style>` tag to an external file.
* Create a directory called `css` at the root of your project
* In this directory, create a file called `main.css`
* Put all the content **between** the `<style>...</style>` tags in this CSS file and save it
* Remove the `<style>` tags altogether
* Add a tag `<link rel="stylesheet" href="css/main.css">` to the `head` of your page.
* Save your page, and confirm in your browser that nothing has changed.
* Commit and do a pull request

## Exercise 2: observe and fix
### Observe
* Open `index.html` in Chrome, and activate the developer tools using whichever way you prefer (inspect element, Ctrl+Alt+I, ...)
* In the Elements panel, click on the `ul` located inside the `nav`. In the Styles panel, notice that there are a bunch
of styles associated to the `ul`, and they are sectioned off.
* At the very bottom, is a grey section called "user agent stylesheet". Right above it, another says `nav ul {...`
and has the styles we defined ourselves.
* The user agent stylesheet is the browser's own opinion about how your HTML should look. Each browser has a slightly
different opinion about it, and the CSS rules in there often use non-official properties such as `-webkit-padding-start`.
* Notice that the `ul` has a property `-webkit-padding-start` set to `40px`. This is what gives it its indentation.
* In the inspector, under the `nav ul` section, add a new property called `padding` and set its value to `0`.
* Notice that the indentation is now gone.

### Fix
* In general, when creating an HTML/CSS based page or site, we want to control our presentation as much as possible.
Instead of manually overriding all the browsers' opinions, we use a **reset** or **normalize** file to add some CSS
that will give us a clean, equal base on all browsers.
* Go to [normalize.css](https://necolas.github.io/normalize.css/), and download the latest version of the normalize CSS file.
* Add this file to the `css` directory of your project, and include it in the `index.html` file.
* Make sure you include the normalize CSS **above** your own CSS. As we will see later on, it turns out that CSS defined
earlier in your document is seen as "less important". External CSS should always be added before your own, to make sure
you have the maximum amount of control.
* Commit and do a pull request

## Exercise 3: inlines and blocks
* Add a background color of your choice to the `nav` element. Notice that the background color only extends up to the **text** of the menu links.
* After reading about the [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) property, change the `display` property
of the **`li`** elements from its current `inline` value to `inline-block`.
* Notice how the background color now extends all the way to the full menu item.
* It turns out that `inline` elements' padding and margins don't affect the surrounding elements. `inline-block`
is the "best of both worlds".
* Add some spacing between the `nav` and its elements using the appropriate property.
* Get rid of the margin added automatically by Chrome to the `ul` that is inside the `nav`.
* Add some spacing between the `nav` and the element that will come after it, using `margin-bottom`.
* Save/commit and do a pull request

## Exercise 4: HTML tables
* Read about [HTML tables on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) or by looking at examples using your google-fu.
* Complete the "Schedule" section of the page so that it looks like this:

Morning | Afternoon
--------|----------
10AM-12PM: class | 1PM-6PM: Practice

* To do this, you'll need to read about the [`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse) CSS property.
* Another way you can go about doing this is by reverse-engineering this HTML page :)
* Commit and do a pull request

## Exercise 5: Fixing up the footer
* Give the footer a black background color, and space out its border from its contents
* Make the text inside the footer white so it can become visible again. **Notice** that you only need to add the `color`
property to the `footer`. It will be **inherited** by all the elements under it, unless they have their own color!
* Notice that the links (`<a>`) don't seem to be changing color. Try to see why, and fix the links, giving them the `tomato`
color and removing their underline.
* Read about the [CSS `float` property on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/float) or by looking at some examples
* Using `float`, make the partners and links section appear next to each other, and each taking 50% of the width of the footer. **HINT**: you might have to *slightly* change the HTML for that
* Fix the partner links so that they appear next to each other, just like the navigation menu at the top
* Without changing the images, fix them in CSS so that they appear to have a width of 100px.
* Commit and do a pull request

## Exercise 6:
Using your newly-acquired HTML and CSS fus, work on the personal page that you created on the first day of class.
Especially, you should be learning about the [new stuff in CSS3](http://www.1stwebdesigner.com/css3-introduction/)
through this link, as well as other resources, using your google-fu. Make this a personal discovery, and concentrate 
only on the aspects that you think would help you build your page. Ask us questions if you are not sure about 
something that you read.

**Remember**: CSS is HUGE! You shouldn't be trying to remember how to do everything, but rather how to find information
about how to do what you want to do.
