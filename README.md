# Theming &amp; Accessibility

DRAFT!

## Requirements

With Dark Mode a hot topic is in the block since 2017. Since 2019 it's default on iOS and Android 10 and suddently it's becomes "standard". The high contrast mode is available since ....
To be truly human-centred we should deliver the design in light mode, dark mode and high contrast. Fortunately Microsoft finally delivers--thanks to Chromium--a true browser with support for media queries.

## Research
* https://drafts.csswg.org/mediaqueries-5/#forced-colors
* https://www.w3.org/TR/css-color-adjust-1/#forced
* https://drafts.csswg.org/css-color/#css-system-colors
* https://drafts.csswg.org/mediaqueries-5/#descdef-media-prefers-color-scheme	
* https://hiddedevries.nl/en/blog/2018-12-24-making-single-color-svg-icons-work-in-dark-mode

The old proprierary attribute where aliased:
-ms-high-contrast to forced-colors
-ms-high-contrast-adjust to forced-colors-adjust
	
## Support
```(-ms-high-contrast: active | black-on-white | white-on-black)```
/*	macOS: not supported;
    Windows: works in IE &amp; Edge if high contrast mode enabled DEPRECATED */
	
```(prefers-color-scheme: dark)```
/*	macOS; works in Safari and Chrome
    Windows: works in Chrome & Chredge if Windows Dark Mode enabeled
		doenst work in Edge */
		
```(forced-colors: active)```
/*	macOS: tbd
		Windows: works in Chredge if high contrast mode enabled */
		
```(prefers-contrast: high)```
	/* https://drafts.csswg.org/mediaqueries-5/#prefers-contrast */

## Windows System High Contrast Colours

```
--color-bg: Canvas; /* Background of application content or documents.*/
--color-text: CanvasText; /* Text in application content or documents.*/
--color-text--link: LinkText; /* Text in non-active, non-visited links.*/
--color-text--visited: VisitedText; /* Text in visited links.*/
--color-text--active: ActiveText; /* Text in active links.*/
--color-action--push: ButtonFace; /* The face background color for push buttons.*/
--color-action--push-text: ButtonText; /* Text on push buttons.*/
--color-action--input: Field; /* Background of input fields.*/
--color-action--input-text: FieldText; /* Text in input fields.*/
--color-action--selection-bg: Highlight; /* Background of item(s) selected in a control.*/
--color-action--selection-text: HighlightText; /* Text of item(s) selected in a control.*/
--color-text--disabled: GrayText; /* Disabled text. (Often, but not necessarily, gray.)*/
```