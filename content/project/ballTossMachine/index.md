+++
# Date this page was created.
date = 2018-10-15T00:00:00

# Project title.
title = "Ball-Toss Machine"

# Project summary to display on homepage.
summary = "Patent-pending actuated and controllable ball-toss machine."

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["prof", "arduino", "mechatronics", "mech-design"]

# Optional external URL for project (replaces project detail page).

# Does the project detail page use math formatting?
math = false

+++

I, along with a team of 2 other engineers, helped develop the ball-toss machine for an M3 Design client. We began with an [off-the-shelf pitching machine](http://www.athlonic.com/products/wheelerdealer) as the foundation and then added or modified features until we had all the functionality required.

While my co-worker designed and fabricated  a 2 degree-of-freedom (DOF) mechanism to enable a controllable pitching window, I focused on developing pitching control. For this, I started by characterizing the existing pitching mechanism which used a simple linear solenoid to pitch the ball. This involved determining operating voltage, peak current, peak current decay (as battery life wore down), and pulse-width-modulation (PWM) for variable force setting.

Once characterized, it became clear that battery power supply would be an issue. As the device was used, power output decayed substantially which would deteriorate the pitching window's consistency. Therefore, I decided to try using a battery charging circuit to continually 'top off' the batteries with charge 




This page is still in development - please see my {{% staticref "files/SiddharthKurwa_Portfolio.pdf"%}}portfolio{{% /staticref %}} in the meantime. Stay tuned for updates soon!