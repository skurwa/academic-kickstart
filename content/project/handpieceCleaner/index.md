+++
# Date this page was created.
date = 2018-09-01T00:00:00

# Project title.
title = "Automated Medical Handpiece Cleaner"

# Project summary to display on homepage.
summary = "Prototype medical device to clean and lubricate medical handpieces."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "avatar.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["prof", "arduino", "mechatronics"]

# Optional external URL for project (replaces project detail page).

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
# [header]
# image = "icon.png"
# caption = "My caption :smile:"

+++

While an intern at M3 Design, I had the unique opportunity of owning the full development of a prototype medical device's control system. The product is intended to clean and lubricate the internals of a client's medical handpieces, improving tool life and sustained quality.

{{< figure src="handpiece.png" title="Medical Handpieces" >}}

To begin, I started by laying out the state machine architecture with a simple breadboarded mock-up using LEDs, switches, pushbuttons, and a display.

{{< figure src="mockUp.png" title="Initial Mock-Up" >}}

With the basic states laid out and control developed, I began integrating physical components - motors, pumps, and sensors. With these physical components, processes within each state could be defined, forming a hierarchical state machine and functional physical form.

{{< figure src="functional.png" title="Functional Prototype" >}}

Physical components also added another layer of complexity with debounce, power supply, overload, and motor control issues. Troubleshooting each one-by-one took time to get right, but it was an excellent way to understand the challenges in transitioning a theoretical idea or mock-up into a physical, useful device. With the physical system, we also worked on tuning the mechanical function of the device. With the mechanical design engineer, I worked to ensure that the pumps were providing the desired fluid pressure head, flowrate, and cycle duration and iteratively tuned the open-loop saturation and gain with sense resistors on the motor driver and control parameters (PWM settings).

{{< figure src="openLoopControl.png" title="Open-Loop Control" >}}

With the mechanical and control functions solved, user interface and experience took center-stage. Working with the team's industrial designer, we determined workflows the user might follow, edge cases, and information to communicate to the user at each stage (alarm notifications and status/state indicators). 

{{< figure src="userWorkflow.png" title="Sample UI Test Case" >}}

With all the pieces (controls, mechanical, UI) figured out, we finally pieced the prototype together for delivery to the client. This particular project was a great experience in negotiating needs/requirements across a cross-functional team (industrial design, mechanical engineering, and controls engineering). The final prototype was a beautiful <i>and functional</i> testament to everyone's hard work and collaboration!

{{< figure src="lookslikeworkslike.png" title="Final Prototype" >}}

Here's a synopsis I presented on my experience with the project.

<div align="center"><iframe src="https://onedrive.live.com/embed?cid=197026BD6A38CBBC&amp;resid=197026BD6A38CBBC%212771&amp;authkey=AO0uB5UsYOg2X5g&amp;em=2&amp;wdAr=1.7777777777777777" width="722px" height="431px" frameborder="0">This is an embedded <a target="_blank" href="https://office.com">Microsoft Office</a> presentation, powered by <a target="_blank" href="https://office.com/webapps">Office</a>.</iframe></div>