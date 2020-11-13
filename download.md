---
layout: default
title: Download
---

# Download

Haven't received your download link?

<form id="fs-frm" name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/signup@ragdolldynamics.com" method="post">
  <fieldset id="fs-frm-inputs">
    <label for="full-name">Full Name</label>
    <input type="text" name="name" id="full-name" placeholder="Rag Doll" required="">
    <label for="email-address">Email Address</label>
    <input type="email" name="_replyto" id="email-address" placeholder="rag@doll.com" required="">
    <label for="message">Message</label>
    <textarea rows="5" name="message" id="message" placeholder="Sign me up!" required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  </fieldset>
  <input type="submit" value="Submit">
</form>

<br>
<br>

# Install

Ragdoll ships as a Maya [Module](https://around-the-corner.typepad.com/adn/2012/07/distributing-files-on-maya-maya-modules.html).

1. Run the `.msi` installer
2. Restart Maya


You should now see a new `Ragdoll` menu.

![image](https://user-images.githubusercontent.com/2152766/95727954-cb353900-0c72-11eb-9592-b7fa930fff3b.png)

For more options, see [Advanced Install](/troubleshooting#advanced-install).

<br>

# Upgrade

The MSI installer currently cannot be used to upgrade, so instead:

1. Unpack the `.zip` to `%USERPROFILE%/Documents/maya`
2. Restart Maya

> Or `~/maya` on Linux

<br>

# FAQ

<blockquote class="faq">What are my workstation requirements?</blockquote>

Anything capable of running Maya can run Ragdoll.

- Windows 10+ or CentOS 7+
- 64-bit Intel® or AMD® processor
- 4 GB of RAM
- Maya 2018-2021

<blockquote class="faq">What are my licensing options?</blockquote>

- `Trial` - 60 days of non-commercial use, no strings attached
- `NodeLocked` - Any number of users, one machine per licence
- `Floating` - Any number of machines, one user per licence
- `Headless` - A cost-effective alternative for distributed simulations

<blockquote class="faq">What happens when my licence runs out?</blockquote>

Your scenes will still open, but the solver will be disabled. Contact [licence@ragdolldynamics.com](mailto:licence@ragdolldynamics.com) for renewal of your licence.

<blockquote class="faq">What happens when I skip frames?</blockquote>

Best not to, you'll see this warning message in your Script Editor.

```bash
Warning: Ragdoll evaluation skipped, frame change too large
```

Letting you know to rewind and not trust the results until you do.

<blockquote class="faq">How do I disable the ground?</blockquote>

A static collider is automatically added on the Maya grid per default, it can be disabled on the `rdScene` node via the `.useGround` attribute.

<blockquote class="faq">Why not use nHair for overlapping animation?</blockquote>

Ragdoll simulates your translate and rotate channels, whereas nHair simulates point geometry. You can convert those points into translation and rotation, but given the choice why would you? Besides, Ragdoll has far more robust collisions, control and constraints than nHair or nCloth could ever hope to achieve, at much greater performance.

<br>

# Limitations

As of `{{site.ragdoll_version}}` these are the current known limitations of Ragdoll.

- Must visit start frame on scene open
- Poor support for the `scale` attribute
- Attributes `jointOrient`, `rotatePivot` and `rotatePivotTranslate` will be zeroed out
- When weight painting rigid joints, cannot right-click "Select influence"
