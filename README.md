
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>permutations_test</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Permutations-Significance-Test">Permutations Significance Test<a class="anchor-link" href="#Permutations-Significance-Test">&#182;</a></h3><p>A common problem that one encounters when analyzing data is the need to compare samples of data, <code>sample_A</code> and <code>sample_B</code> in our case, in order to determine whether or not the observed samples are drawn from the same parent probability density functions. Are the two samples that you are analyzing actually different from one another? One way to test for differences is to make some theoretical assumptions about the nature of the probability function of the null hypothesis. For example, if the null hypothesis is normally distributed then we can look at our observed samples and make some educated inferences about whether they are drawn from the same theoretcial null hypothesis distribution. It is often difficult to be confident in theoretical assumptions about your particular set of data. Often I find myself analyzing problem sets in which the underlying probability functions are not well understood, and do not lend themselves easily to theoretical assumptions. In these cases I use permutations testing. I have found this test to be practical, intuitive, and reasonably easy to implement with a little bit of custom code. I want to share my use of this test with you because I think it is powerful and widely applicable.</p>
<h5 id="Intuition-and-Terminology">Intuition and Terminology<a class="anchor-link" href="#Intuition-and-Terminology">&#182;</a></h5><p>Ok...permutations test. Well, permutations of what? The testing name refers to permutations of the null hypothesis. The null hypothesis is the hypothesis that your two observed samples are drawn from the same parent distribution and there are no significant differences between them. Under the null hypothesis, your two samples are two ways the null hypothesis could be observed. In other words they are two permutations of samples from the same larger parent distribution. If it is in fact true that we have two observed samples from the null hypothesis distribution, then we can create many more observations using re-sampling techniques. An assumption that must be met in order for a permutations test to be applicable is the observed data points must be exchangeable between the observed sample groups. In practice this means that there can't be any underlying reason why an observation in <code>sample_A</code> couldn't have also occured in <code>sample_B</code>. You can test any feature of the data that your wish including, mean difference, deviation, or t-score. For this purpose I will use the mean difference between the two samples.</p>
<h5 id="Steps-and-Methods">Steps and Methods<a class="anchor-link" href="#Steps-and-Methods">&#182;</a></h5><p>The steps to perform a permutations test are as follows:</p>
<ol>
<li>Compare and log the observed mean difference between <code>sample_A</code> and <code>sample_B</code>.</li>
<li>Pool/Merge the observed data points from <code>sample_A</code> and <code>sample_B</code> into one set of data <code>null_observation</code>.</li>
<li>Recreate the two groups by randomly sampling without replacement from <code>null_observation</code> creating two new groups, <code>resample_A</code> and <code>resample_B</code>, and log the mean difference between the two resampled groups.</li>
<li>Repeat step 3 n times. In our case we will re-sample the data 1000 times.</li>
<li>Compare the mean differences collected from <code>resample_A</code> and <code>resample_B</code> to the mean difference obtained in step 1.</li>
</ol>
<h5 id="Example">Example<a class="anchor-link" href="#Example">&#182;</a></h5>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Using the numpy normal distribution function where loc is the mean, </span>
<span class="c1"># scale is the standard deviation, and size is the number of observations.</span>

<span class="n">n_observations</span> <span class="o">=</span> <span class="mi">1000</span>


<span class="c1"># Make the distributions non-equal to see if the permutations test</span>
<span class="c1"># shows the difference.</span>
<span class="n">sample_A</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">normal</span><span class="p">(</span>
    <span class="n">loc</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> 
    <span class="n">scale</span><span class="o">=</span><span class="mf">0.1</span><span class="p">,</span> 
    <span class="n">size</span><span class="o">=</span><span class="n">n_observations</span><span class="p">,</span>
<span class="p">)</span>

<span class="n">sample_B</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">normal</span><span class="p">(</span>
    <span class="n">loc</span><span class="o">=</span><span class="mf">1.1</span><span class="p">,</span> 
    <span class="n">scale</span><span class="o">=</span><span class="mf">0.1</span><span class="p">,</span>
    <span class="n">size</span><span class="o">=</span><span class="n">n_observations</span><span class="p">,</span>
<span class="p">)</span>

<span class="n">observed_mean_difference</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">sample_A</span><span class="p">)</span> <span class="o">-</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">sample_B</span><span class="p">)</span>
<span class="n">null_observation</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">concatenate</span><span class="p">((</span><span class="n">sample_A</span><span class="p">,</span> <span class="n">sample_B</span><span class="p">))</span>

<span class="c1"># Print the shapes of the above arrays to make sure everything is as expected</span>
<span class="nb">print</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">sample_A</span><span class="p">),</span><span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">sample_B</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">shape</span><span class="p">(</span><span class="n">null_observation</span><span class="p">))</span>

<span class="k">def</span> <span class="nf">resample</span><span class="p">(</span><span class="n">input_array</span><span class="p">,</span> <span class="n">output_size</span><span class="p">,</span> <span class="n">n</span><span class="p">):</span>
    
    <span class="n">sample_mean_differences</span> <span class="o">=</span> <span class="p">[]</span>
    
    <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
        <span class="c1"># Shuffle the null_observation array using numpy suffle method</span>
        <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">shuffle</span><span class="p">(</span><span class="n">input_array</span><span class="p">)</span>

        <span class="n">resample_A</span><span class="p">,</span> <span class="n">resample_B</span> <span class="o">=</span> <span class="n">input_array</span><span class="p">[:</span><span class="n">output_size</span><span class="p">],</span> <span class="n">input_array</span><span class="p">[</span><span class="n">output_size</span><span class="p">:]</span>

        <span class="n">sample_mean_differences</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">resample_A</span><span class="p">)</span> <span class="o">-</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">resample_B</span><span class="p">))</span>
    
    <span class="k">return</span> <span class="n">sample_mean_differences</span>

<span class="n">sample_mean_differences</span> <span class="o">=</span> <span class="n">resample</span><span class="p">(</span>
    <span class="n">input_array</span><span class="o">=</span><span class="n">null_observation</span><span class="p">,</span>
    <span class="n">output_size</span><span class="o">=</span><span class="n">n_observations</span><span class="p">,</span>
    <span class="n">n</span><span class="o">=</span><span class="mi">1000</span>
<span class="p">)</span>

<span class="n">significance_cutoff</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">percentile</span><span class="p">(</span>
    <span class="n">sample_mean_differences</span><span class="p">,</span> <span class="mi">99</span>
<span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">30</span><span class="p">,</span><span class="mi">20</span><span class="p">))</span>

<span class="n">plot</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span> 
    <span class="n">a</span><span class="o">=</span><span class="n">sample_mean_differences</span><span class="p">,</span>
    <span class="n">bins</span><span class="o">=</span><span class="mi">10</span>
<span class="p">)</span>

<span class="n">plot</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span>
    <span class="n">x</span><span class="o">=</span><span class="n">observed_mean_difference</span><span class="p">,</span> 
    <span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> 
    <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;-.&#39;</span>
<span class="p">)</span>

<span class="n">plot</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span>
    <span class="n">x</span><span class="o">=</span><span class="n">significance_cutoff</span><span class="p">,</span> 
    <span class="n">color</span><span class="o">=</span><span class="s1">&#39;green&#39;</span><span class="p">,</span> 
    <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;--&#39;</span>
<span class="p">)</span>

<span class="n">plot</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span>
    <span class="n">x</span><span class="o">=-</span><span class="n">significance_cutoff</span><span class="p">,</span> 
    <span class="n">color</span><span class="o">=</span><span class="s1">&#39;green&#39;</span><span class="p">,</span> 
    <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;--&#39;</span>
<span class="p">)</span>

<span class="c1"># The red line is the observed mean difference. The green lines </span>
<span class="c1"># are the 99th percentile significance cutoffs. If the red line</span>
<span class="c1"># lies between the two green lines then the observed results </span>
<span class="c1"># are not significant. If the red line lies outside the green</span>
<span class="c1"># lines then the observed results are significant at p&lt;=0.01.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(1000,) (1000,) (2000,)
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt output_prompt">Out[35]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.lines.Line2D at 0x126087278&gt;</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h5 id="Final-Thoughts">Final Thoughts<a class="anchor-link" href="#Final-Thoughts">&#182;</a></h5><p>The above test can be run numerous times to get an idea of how often the results will be significant. 
You can use this example to explore the results of the permutations test. Set the <code>sample_A</code> and <code>sample_B</code> distributions to be equal to each other to see what the results of the permutations test will show.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
