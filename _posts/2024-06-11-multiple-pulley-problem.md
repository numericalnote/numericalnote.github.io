---
title: Multiple Pulley Problem
author: Karthik
date: 2024-06-11 02:08:00 -0500
categories: [Physics]
tags: [Multiple Pulley Problem]
render_with_liquid: false
math: true
---

# Introduction to Multiple Pulley Problems

When making the jump from AP Physics 1 to olympiad level, one of the
most important concepts to add on in regards to newtons' laws of motion
are multiple pulley problems. In order to understand how to solve
questions looking like this:

![image](https://i.ibb.co/rvDy5bJ/1.png)

# Frame of Reference 

It is necessary to first understand the concept of frame of reference.
If a car is speeding up, take: (1) an observer in the car and (2) an
observer outside the car. The car is not accelerating in the frame of
the car (relative to the car), but the car is accelerating with respect
to the ground (speeding up).

# Explaining the Single Pulley

While this may not seem immediately relevant, let's take a closer look
at a single pulley.

![image](https://i.ibb.co/kXdpgqq/2.png)

In problems such as this, one might wonder why the acceleration of mass
m and M are the same in magnitude. Here is the deal, since the pulley is
fixed, the amount of string is constant. So if mass M goes down by a
distance x, mass m has to rise by that much x in order to keep the
length of string conserved. Since they both initially are at rest and
have the same time period, $$\Delta x = v_{0}t + \frac{1}{2}at^{2}$$
They will have the same acceleration, although in opposite directions
clearly.

# Constraint Equation in Pulley systems: 

However, the tricky part begins here

![image](https://i.ibb.co/2KRdn1g/3.png)

## Method 1: 

Sure, in the fixed pulley, the string that goes up has to go down cool.
But at the most right in the system of two pulleys, imagine the force
pulling on the right part of the string. Due to this, the left pulley
will raise as it is the load for the right pulley. However, the left
pulley has two strings above it, so if the left pulley moves up by a
distance $x$, $2x$ of string is lost. Therefore, for string to be
conserved, the right part of the string has to move $2x$. Thus, assuming
the masses are initially at rest and employing kinematics, it becomes
clear that the acceleration of the right most string is $2a$, while the
parts of the string above the left pulley are accelerating upwards at
$1a$. Whatever distance the left pulley raises is taken by the load, so
the load and the left pulley have the same acceleration. This is how you
would write a constraint equation. Instead of there existing a applied
force on the right end of the system of two pulley, lets say there was a
mass instead and the system accelerated due to its gravitational force.
Lets also call the load mass 1 and mass on the right mass 2.\
We can say acceleration of mass 2 =
$2 \cdot \text{ acceleration of mass } 1$. This method of thinking
regarding string conservation is a common method to write the constraint
equation.

## Method 2:

What if we take the frame of reference of an observer on top of the
pulley. The pulley is not accelerating relative to the pulley. If the
pulley is not accelerating in this frame, the two strings have the same
acceleration relative to the pulley.

$$a_{1p} = -a_{2p}$$ $$a_{1} - a_{p} = -a_{2} + a_{p}$$
$$a_{p} = \frac{(a_{1} + a_{2})}{2}$$ Therefore, the acceleration of the
pulley can always be determined by taking the average of the two strings
attached to it. In the problem above, the pulley is fixed so $ap = 0$.
$a_{1} = a_{2}$ follows from this formula for this specific case.
Applying it to the question above, we note the right pulley to be fixed,
so if we let the acceleration of the rightmost string be $a_2$. Then,
the left string attached to the pulley is $-a_2$. In the left pulley,
the left string is attached to the ceiling, so it is $0$. The pulleys
acceleration is $-\dfrac{a_{2}}{2}$. Since the load will have the same
acceleration, the acceleration of the load = $-\dfrac{a_{2}}{2}$.

# How to Attack Pulley System Problems 

1.  Write the net force equations for each of the masses.

2.  Write the constraint equation, relating the masses' accelerations.
    Note: This is extremely important as unlike the single pulley
    system, the masses may and most of the time will have different
    accelerations.

3.  Substitute and solve.

# Writing the Net Force Equation 

In order to solve this problem, we need to use two guiding principles.

1.  Pulleys are assumed to be massless in most problems. By newtons
    second law, the net force on the pulleys are 0.\

2.  Since a string is massless, the tension is constant throughout.

Looking at the problem, first draw it without the masses and label it to
find out the tensions.

<figure style="display: flex; align-items: flex-start;">
    <img src="https://i.ibb.co/YdTjCcx/4.png" />
    <img src="https://i.ibb.co/mSTb9m2/5.png" />
</figure>


How to do this: At the right end, let the tension in the string be $T$.
Since the tension throughout the entire string is $T$, we can say the
tension in the two strings above left upper pulley are also $T$. Since
the net force on the left upper pulley is 0, this means that the tension
in the string right below it is $2T$. Let the tension of the string in
left bottom pulley be $x$. Since the netforce on the left bottom pulley
is 0, $2T-2x = 0$, so $x = T$.

$$T - m_{1}g = m_{1}a_{1}, \quad a_{1} = \frac{T}{m_{1}-g}$$
$$T - m_{2}g = m_{2}a_{1}, \quad a_{2} = \frac{T}{m_{2}-g}$$
$$T - m_{3}g = m_{3}a_{3}, \quad a_{3} = \frac{T}{m_{3}-g}$$

# Writing the Constraint Equation 

Apply method 2. Letting m1's acceleration be $a1$ and since the upper
right pulley is fixed, the left string attached to the pulley will have
acceleration -$a1$. Looking at the upper left pulley, the left string is
attached to the ceiling, so its acceleration is 0. Therefore, the
acceleration of the upper left pulley is $\frac{-a_{1}}{2}$. Since the
distance traveled by the lower left pulley is the same as the upper left
pulley, they have the same acceleration. Therefore, the acceleration of
the lower left pulley is $\frac{-a_{1}}{2}$. Letting $M2$ and $M3$ have
accelerations $a2$ and $a3$ respectively, we get the formula
$\frac{-a_{1}}{2} = \frac{a_{2} + a_{3}}{2}$. This gives us the
constraint equation $a_1 + a_2 + a_3 = 0$. To then solve the problem,
substitute $a1, a2, a3$ from the netforce equations into the constraint
equation and solve.

# Final Remarks 

In order to solve problems such as these, it is necessary to do a lot of
practice with different variations of the problems. More problems can be
found in HC Verma's Concept of Physics - amazing book and David Morin's
Problems and Solutions in Introductory Mechanics. I apologize if I have
made any mistakes in the presentation of this topic. Feel free to
contact me at <vsaikarthik@outlook.com> to clarify doubts, point out any
errors, or request a topic.
