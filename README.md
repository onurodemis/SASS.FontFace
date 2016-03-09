# SASS.FontFace
Easy implementation font face and glyphicons with SASS

http://onurodemis.com/SASS.FontFace/

How to use
Folder Structure

- Assets
- -- \Css
- -- \Fonts
- ---- \FontName
- ------FontName.eot
- ------FontName.ttf
- ------FontName.woff
- ------FontName.svg
- -- Sass
- ------ main.scss
- ------_glyphicons.scss
- ------ \Mixins
- --------_common.scss
- --------_font-face-mixins.scss
- --------_font-face-settings.scss


>Import Font Face Settings and Mixins

@import "Mixins/font-face-settings";

@import "Mixins/font-face-mixins";

>Import Glyphicons Classes that generated via IcoMoon

@import "glyphicons";

>Your Theme

$theme-fonts:
    (fn, FontName),
    (fn2, FontName2)
;

Create Fonts
@include create-font-face($theme-fonts);


Create Glyphicons
If you embed Font Awesome, you can set prefix param 'fa'. 

For example: @include create-gli('Glyphicons', fa);

Default prefix name is 'icon' this prefix is generally using by IcoMoon.
@include create-gli('GliFontName');


In Conclusions
You can extend and use auto generated class from your new classes
For example

body {
  @extend .fn;
}
