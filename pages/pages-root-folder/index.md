---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: headers/gym_h2.jpg

widget1:
  title: "Workout of the Day"
  url: "#wod"   #'/blog/'
  image: showcase/whats_crossfit.jpg
  text: 'Anticipating the unknown? <br/>Checkout today''s WOD now...'
widget2:
  title: "The Open is coming."
  url: '/schedule/'
  text: 'Are you prepared?<br/><br/>Train now.'
  video: '<a href="#" data-reveal-id="videoModal"><img src="http://img.youtube.com/vi/skUxFsTzZ4Q/sddefault.jpg" width="302" height="200" alt=""/></a>'
  # widget2's video call the video script below
  # How to get YouTube thumbnails: https://gist.github.com/protrolium/8831763
widget3:
  title: "Join Us"
  url: '/info/'
  image: showcase/wod1.jpg
  text: '"Be impressed by intensity, not volume." <cite>Coach Glassman</cite>'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://github.com/ohjho/asphodel2018/issues/new
  text: Found an issue with this BETA site? Log it ›
  style: success
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/skUxFsTzZ4Q" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
