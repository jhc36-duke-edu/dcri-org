<style>
img {
	max-width:99%;
}
a {
  color: blue;
}
pre {
  font: inherit;
  word-wrap: break-word;
  background: none;
  border: none;
}
</style>

# DCRI.org Contact Page Assessment



<details>
<summary>__Table of Contents__</summary>

[toc]

</details>


## Contact form improvement suggestions

The contact form on this website is pretty good, but there are a few suggestions that could make it a little more user friendly to screen reader users.

Here is a nice recource to [learn more about contact form accessibility on w3.org](https://www.w3.org/WAI/tutorials/forms/notifications/)

###Demo of using the form with a screen reader:

(To get the full effect, watch the video with your eyes closed.)

<video controls title="demo of using the form with a screen reader.">
  <source src="assets/dcri-contact-form-sml.mp4" type="video/mp4">
Your browser does not support the video tag.
</video> 

It would be possible for a screen reader user to figure out the form with a little difficulty. It might be possible to make some easy improvements.

###Suggested improvements:

Change the heading above the form from "Learn More" to "Contact Form" 

I'm not sure how the form is generated, or DCRI.org has control over the form. Changing the error messages would be helpful.

If changes can be made, making the messages more specific would be a big help.  The Email field already has great error messages. But all the other fields use the same message, which would make it very difficult for them to identify the error location and recover from the error.

```html
<span role="alert" class="wpcf7-not-valid-tip">
  The field is required.
</span>
```
Adding the name of the missing field would fix the issue.

```html
<span role="alert" class="wpcf7-not-valid-tip">
  The Message field is required.
</span>
```

__[Please view Gist](https://gist.github.com/jhc36-duke-edu/81b6a0dffd84f78e778e9e45115ba6cc/revisions)__
<hr>
<br>
<br>

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