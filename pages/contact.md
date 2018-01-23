---
layout: page
title: "Contact Us"
subheadline: "we are open seven days a week."
teaser: ""
header: no
permalink: "/contact/"
---
The box's address:  
[ Shop 11, {{site.address}}][1]

Nearest MTR- **HKU Station _Exit C2_**

You can also call **_(+852) 3568-7719_**

Email us at [{{site.contact_email}}](mailto:site.contact_email) or use the contact form below:

<div class="row">

    <div id="contactForm" class="small-8 medium-8 large-8 columns">
      <form id="myForm" method="post" action="https://formspree.io/{{site.contact_email}}" data-abide>  

          <h5>Contact Us</h5>
          <label>Name</label>
          <small class="error">Your full name is required.</small>
          <input type="text" placeholder="Full Name" name="name" required>

          <label>Email</label>
          <small class="error">An email address is required.</small>
          <input type="email" placeholder="username@address.com" name="replyto" required>

          <label>Your Message</label>
          <small class="error">Your message is required.</small>
          <textarea rows="9" placeholder="Enter your message here" name="message" required></textarea>

        <input type="submit" class="nice blue radius button" value="Send Message">
        </form>
    </div><!--end 8 columns-->
</div>
[1]: https://www.google.com.hk/maps/search/?api=1&query={{site.address}}
