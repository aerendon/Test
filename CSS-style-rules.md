##CSS Style Rules
###CSS Validity
Use valid CSS where possible.

Unless dealing with CSS validator bugs or requiring proprietary syntax, use valid CSS code.

Use tools such as the [W3C CSS validator](http://jigsaw.w3.org/css-validator/) to test.

Using valid CSS is a measurable baseline quality attribute that allows to spot CSS code that may not have any effect and can be removed, and that ensures proper CSS usage.

###ID and Class Naming
Use meaningful or generic ID and class names.

Instead of presentational or cryptic names, always use ID and class names that reflect the purpose of the element in question, or that are otherwise generic.

Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.

Generic names are simply a fallback for elements that have no particular or no meaning different from their siblings. They are typically needed as “helpers.”

Using functional or generic names reduces the probability of unnecessary document or template changes.

```CSS
/* Not recommended: meaningless */
#yee-1901 {}

/* Not recommended: presentational */
.button-green {}
.clear {}
```
```CSS
/* Recommended: specific */
#gallery {}
#login {}
.video {}

/* Recommended: generic */
.aux {}
.alt {}
```

###ID and Class Name Style
Use ID and class names that are as short as possible but as long as necessary.

Try to convey what an ID or class is about while being as brief as possible.

Using ID and class names this way contributes to acceptable levels of understandability and code efficiency.
```CSS
/* Not recommended */
#navigation {}
.atr {}
```
```CSS
/* Recommended */
#nav {}
.author {}
```
###Type Selectors
Avoid qualifying ID and class names with type selectors.

Unless necessary (for example with helper classes), do not use element names in conjunction with IDs or classes.

Avoiding unnecessary ancestor selectors is useful for [performance reasons](http://www.stevesouders.com/blog/2009/06/18/simplifying-css-selectors/).
```CSS
/* Not recommended */
ul#example {}
div.error {}
```
```CSS
/* Recommended */
#example {}
.error {}
```
###Horthand Properties
Use [shorthand properties](http://www.w3.org/TR/CSS21/about.html#shorthand) where possible.

CSS offers a variety of shorthand properties (like `font`) that should be used whenever possible, even in cases where only one value is explicitly set.

Using shorthand properties is useful for code efficiency and understandability.
```CSS
/* Not recommended */
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
```
```CSS
/* Recommended */
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```
###0 and Units
Omit unit specification after “0” values.

Do not use units after 0 values unless they are required.
```CSS
margin: 0;
padding: 0;
```
###Leading 0s
Omit leading “0”s in values.

Do not use put 0s in front of values or lengths between -1 and 1.
```CSS
font-size: .8em;
```
###Hexadecimal Notation
Use 3 character hexadecimal notation where possible.

For color values that permit it, 3 character hexadecimal notation is shorter and more succinct.
```CSS
/* Not recommended */
color: #eebbcc;
```
```CSS
/* Recommended */
color: #ebc;
```
###Prefixes
Prefix selectors with an application-specific prefix (optional).

In large projects as well as for code that gets embedded in other projects or on external sites use prefixes (as namespaces) for ID and class names. Use short, unique identifiers followed by a dash.

Using namespaces helps preventing naming conflicts and can make maintenance easier, for example in search and replace operations.
```CSS
.adw-help {} /* AdWords */
#maia-note {} /* Maia */
```
###ID and Class Name Delimiters
Separate words in ID and class names by a hyphen.

Do not concatenate words and abbreviations in selectors by any characters (including none at all) other than hyphens, in order to improve understanding and scannability.
```CSS
/* Not recommended: does not separate the words “demo” and “image” */
.demoimage {}

/* Not recommended: uses underscore instead of hyphen */
.error_status {}
```
```CSS
/* Recommended */
#video-id {}
.ads-sample {}
```
###Hacks
Avoid user agent detection as well as CSS “hacks”—try a different approach first.

It’s tempting to address styling differences over user agent detection or special CSS filters, workarounds, and hacks. Both approaches should be considered last resort in order to achieve and maintain an efficient and manageable code base. Put another way, giving detection and hacks a free pass will hurt projects in the long run as projects tend to take the way of least resistance. That is, allowing and making it easy to use detection and hacks means using detection and hacks more frequently—and more frequently is too frequently.






