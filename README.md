Angular Sticky
==============

A simple, pure javascript (No jQuery required!) AngularJS directive to make elements stick when scrolling down.

### Features

  * Allows use of an offset so elements can be sticked to ej. 50px from the top of the browser
  * Recalculates element position on page load and on window resize
  * Clean: No classes are added, no jQuery is required, no CSS files or configuration is needed.


### Bower

Install with bower with:

```bash
bower install ngSticky
```


### Usage

Include the .js file in your page then enable usage of the directive by including the "sticky" module
as a dependency. Use the directive as follows:

    <div sticky> Hey there! </div>

To make the element stick within a certain offset of the top of the screen, you can provide an offset as follows:

    <div sticky offset="100"> I won't touch the top of your screen! </div>

If you want to customize the style while the element is sticky, we have an api for you too:

    <div sticky offset="100" sticky-class="imSoSticky"> Taste my gule! </div>

And if you want to customize the body style while the element is sticky:

    <div sticky offset="100" body-class="somethingIsSticky"> Taste my gule! </div>

In order to enable sticky based on a media query:

    <div sticky media-query="min-width: 768px"> Won't be sticky on small screens! </div>

And if you want to confine an element to it's parent, and let it 'bottom out' just add the confine attribute:

    <div sticky offset="100" confine="true"> Will unstick and stick to bottom of parent element</div>

> NOTE: The confine attribute will automagically assign it's parent a position: relative style in order to help with absolute positioning relative to the parent.
 
Cheers.


###Update (WIP)

To make your sticky elements sticky one after another use:
<div sticky ensure-Offset="true"> Will offset with previous elements heights </div>

> NOTE: Still works bad with anchor bottom


If you want to customize the style while the element is sticky and amount of sticky elements is more than some value use:
<div sticky  compact-On-Count="1" compact-Class="CompactClass">I will change size (initially become smaller) when there are more then 1 elements sticky</div>


If you want to customize the style while the element is sticky and you scrolled some particullar amount use:
<div sticky  compact-Offset="800px" compact-Class="CompactClass">I will change size (initially become smaller) when page scrolled more then 800px </div>