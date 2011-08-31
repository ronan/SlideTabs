SideTabs for jQuery UI
------------------------------------------
© Ronan Dowling - Gorton Studios 
gortonstudios.com
Licenced under the GPL v2

SlideTabs is a jQuery UI plugin that provides a set of tabs where the the content
panel slides in from the side.

SlideFlow is a Coverflow-like effect based on the same base code.

Requirements
jQuery and jQuery UI (ui.core.js)

Usage
html:
<div id="tab-wrapper">
  <ul class="tabs">
    <li><a href="#t1">Tab 1</a></li>
    <li><a href="#t2">Tab 2</a></li>
    <li><a href="#t3">Tab 3</a></li>
  </ul>
  <div class="panels">
    <div id="t1">This is tab 1</div>
    <div id="t1">This is tab 2</div>
    <div id="t1">This is tab 3</div>
  </div>
</div>

javascript:
$('#tab-wrapper').slidetabs({
    tabs:   '.tabs a',
    items:  '.panels > div'
  }
);

Other Options
{
  animate: true,            // Should the tabs animate (slide)?
  duration: 500,            // How fast should the animation be?
  autoRotate: false,        // How long before automatically moving to next tab. Set to false to not auto-rotate.
  loop: false,              // When the tabs get to the end, loop around to the start (for auto-rotate and next/prev buttons).
  rowWidth: 1000,           // How many items before creating a new row of items. Set to 1 to have tabs slide vertically.
  updateURL: true,          // Should switching tabs update the URL (allows refreshes, linking to a specific tab)
  scrollSettings: {
    'duration': 500,        // How fast should the sliding be?
    'axis': 'xy'            // Slide on both axes?
  },
  resizeSettings: {
    'duration': 500         // The outer wrapper will automatically resize to fit the height of each tab. This is the speed of that animation.
  },
  swipe: false,             // Allow iOS swipe gestures (future feature).
  prevnext: false           // Add previous and next links.
}