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

# FAQ

> What are the workstation requirements?

- Windows 10+ or CentOS 7+
- 64-bit Intel® or AMD® processor
- 4 GB of RAM
- Maya 2018-2021

> What are the licensing options?

- **Trial Licence** - Enjoy the full power of the Ragdoll for 60 days, no strings attached
- **Node-locked Licence** - Any number of users, one machine per licence
- **Floating Licence** - Any number of machines, one user per licence

> What happens when my licence runs out?

Your scenes will still open, but the solver will be disabled. Contact mailto:licence@ragdolldynamics.com for renewal of your licence.

<br>

# Limitations

As of `2020.10.07` these are the current known limitations of Ragdoll.

- Save often. It *may*, on rare occasions, crash Maya.
- Only 1 Ragdoll scene may exist per Maya scene
- Only 1 CPU core is used
- Poor support for the `scale` attribute
- Attributes `jointOrient`, `rotatePivot` and `rotatePivotTranslate` will be zeroed out
- Joint X-axis must point towards child joint
- When weight painting rigid joints, cannot right-click "Select influence"
- Must visit start frame on scene open
- Serial/Parallel partially supported, rewinding and constraints doesn't draw correctly 
