<style>
img {
	max-width:99%;
}

pre {
  font: inherit;
  word-wrap: break-word;
  background: none;
  border: none;
}
</style>

# DCRI.org Who We Are Assessment



<details>
<summary>__Table of Contents__</summary>

[toc]

</details>


## Background and foreground colors do not have a sufficient contrast ratio.
Low-contrast text is difficult or impossible for many users to read. [Learn more](https://dequeuniversity.com/rules/axe/2.2/color-contrast?application=lighthouse).


### Purple call out area

This is not a real issue. It is actually a false positive. The white on purple is acequate. However, false positives have been used in litigation to support claims of innaccessible websites.  The fix for this is literally one line of code, so it is worth fixing the false positive.

####Visual location:
![purple call out area](assets/dcri-purple-callout.png)

####HTML location:

```html
<a href="http://www.dcri.org/about/dcri-faculty/" aria-label="opens in new tab">View Our Faculty</a>
```

####Suggested solution:

Leave the background-image as it is.  Change the background-color to one that registers as having a 4.5:1 contrast ratio.

\#FFFFFF on \#767676 = 4.5:1

```css
/* inline photo callout boxes */
.photo-background-image {
background: #767676 url(/wp-content/uploads/2016/10/purpleBlend.png) top left no-repeat;}
```
__[Please view Gist](https://gist.github.com/jhc36-duke-edu/6a33b9a5d804da05af5cfb57c52ed0a2/revisions)__




<details>
<summary>__Additional debugging details__</summary>

_Selector path:_ <br>
`[u'.button.orange > a[href$="dcri-faculty/"]']`

_DOM path:_ <br>
`1,HTML,1,BODY,3,DIV,3,MAIN,1,DIV,0,DIV,0,ARTICLE,2,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,0,DIV,3,DIV,0,DIV,0,A`
</details>
<br>
<br>
<hr>


## The page has a logical tab order
Tabbing through the page follows the visual layout. Users cannot focus elements that are offscreen. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#start_with_the_keyboard).

Success.

<hr>
<br>
<br>
## Interactive controls are keyboard focusable
Custom interactive controls are keyboard focusable and display a focus indicator. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#start_with_the_keyboard).

Success.

<hr>
<br>
<br>


## The user's focus is directed to new content added to the page
If new content, such as a dialog, is added to the page, the user's focus is directed to it. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#start_with_the_keyboard).

Success.
<hr>
<br>
<br>
## User focus is not accidentally trapped in a region
A user can tab into and out of any control or region without accidentally trapping their focus. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#start_with_the_keyboard).

Success.
<hr>
<br>
<br>
## Custom controls have associated labels
Custom interactive controls have associated labels, provided by aria-label or aria-labelledby. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#try_it_with_a_screen_reader).

Success.
<hr>
<br>
<br>
## Custom controls have ARIA roles
Custom interactive controls have appropriate ARIA roles. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#try_it_with_a_screen_reader).

Success.
<hr>
<br>
<br>
## Visual order on the page follows DOM order
DOM order matches the visual order, improving navigation for assistive technology. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#try_it_with_a_screen_reader).

Success.
<hr>
<br>
<br>
## Offscreen content is hidden from assistive technology
Offscreen content is hidden with display: none or aria-hidden=true. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#try_it_with_a_screen_reader).

Success.
<hr>
<br>
<br>
## Headings don't skip levels
Headings are used to create an outline for the page and heading levels are not skipped. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#take_advantage_of_headings_and_landmarks).

Success.
<hr>
<br>
<br>
## HTML5 landmark elements are used to improve navigation
Landmark elements (`<main>, <nav>, etc.`) or ARIA roles are used to improve the keyboard navigation of the page for assistive technology. [Learn more](https://developers.google.com/web/fundamentals/accessibility/how-to-review#take_advantage_of_headings_and_landmarks).

Success.
<hr>
<br>
<br>