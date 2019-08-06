+++
# Date this page was created.
date = 2018-12-02T00:00:00

# Project title.
title = "Smart Cart"

# Project summary to display on homepage.
summary = "Independent research project to prototype a motorized, obstacle avoiding, Arduino-controlled shopping cart."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "avatar.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["academic", "arduino", "mechatronics", "mech-design", "control-systems"]

# Optional external URL for project (replaces project detail page).

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
# [header]
# image = "icon.png"
# caption = "My caption :smile:"

+++

Note: Please review my {{% staticref "files/SiddharthKurwa_SmartCartReport.pdf"%}}final report{{% /staticref %}} and/or {{% staticref "files/SiddharthKurwa_SmartCartPoster.pdf"%}}research poster{{% /staticref %}} for full details of this project. 

The Smart Cart was a project I pursued in my senior year to test my capacity and interest for independent research. To start, I prepared and submitted a proposal to the Department of Mechanical Engineering that identified a project advisor - Dr. Carolyn Seepersad, outlined the project scope, and estimated the necessary budget and timeline.

With Dr. Seepersad's support after reviewing the proposal, I began pursuing the project to design and prototype a shopping cart that could navigate a grocery store. The stretch goal was for the cart to follow a user around the store, but the minimum technical requirements I imposed on myself for the semester was to design the cart to carry a 25 lbf payload, implement motor control, and develop an obstacle avoidance strategy.

Major tasks involved mechanical design, electrical design, and controls development.

I initially started with the mechanical prototype by analyzing a viable drive system to carry the 25 lbf payload, designing the system using SolidWorks, and prototyping the design. The final design after iterating through SolidWorks is shown below.

{{< figure src="CAD.png" title="Mechanical Design" >}}

For electrical design, I decided to use a distributed computing network over the I2C communication protocol. By using a network, I could dedicate individual Arduinos to collecting encoder clicks with interrupts and minimize the risk of missing interrupts as the motor's encoders could click at 3500 Hz at walking speed. Further, the ultrasonic proximity sensors I selected for the obstacle avoidance task required using a delay between the trigger and the echo. This delay would slow down the loop rate of the Arduino (in an undistributed architecture) substantially, causing missed encoder signals and inaccurate wheel velocity measurements for speed control. The distributed network allowed tasks to be managed at asynchronous loop rates and requested on-demand. The planned communication architecture is shown below.

{{< figure src="distributedComputing.png" title="Communications Architecture" >}}

The other major task was to develop the control strategy for motor control and obstacle avoidance. I had chosen to use ultrasonic sensors, encoders, and a compass as my sensor inputs. Input from these sensors could be used to manage the decision-making of the system. First, I laid out the architecture in a function block diagram. 

{{< figure src="functionDiagram.png" title="Control Strategy" >}}

With the PIDs from the block diagram implemented in the Arduino, the next step was to give the controller a way to determine heading and speed setpoints based on environmental factors (obstacle avoidance). To do this, I first simplified the task by assuming that the cart should go forward by default unless an obstacle is detected in its path. Once an obstacle is detected, a decision must be made to pass the obstacle. This strategy is depicted in the following graphic.

{{< figure src="obstacleAvoidance.png" title="Obstacle Avoidance" >}}

At the conclusion of the semester, this project has given me comprehensive exposure and confidence in independently taking a smart product concept from ideation to prototype - a true testament to my four-year engineering education at the University of Texas at Austin! In particular, this project has inspired me to wopursue a career with early-stage prototyping of smart products and pursue graduate school to enhance my core skills and theoretical knowledge of human-machine interaction.