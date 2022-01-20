---
layout: project
type: project
image: images/micromouse.jpg
title: Euler's Method
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2015-07-01
labels:
  - Java
  - Calculus
summary: A handfull of friends and myself were tired of having to repeatedly write out all of our work in order to get the final answer for Euler's Method in Calculus, so we created a small program to instantly get the calculated answer without the hassle!
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```java
// Euler's Method for Differential Equation
import java.io.*;

public class EulerMethod {
   // Consider a differential equation
   double func(double x, double y)
   {
       /* Put formula here (if you need to do something like 15x^2 - 3x^2y, 
        * plug it in like this: ((15 * (x * x)) - ((3 * (x * x)) * y))
        */
       return ((15 * (x * x)) - ((3 * (x * x)) * y));
   }

   // Function for Euler formula
   void euler(double x0, double y, double h, double x)
   {
       double temp = 0;

       // Iterating till the point at which we need approximation
       while (x0 < x) {
           temp = y;
           y = y + h * func(x0, y);
           x0 = x0 + h;
       }

       System.out.println("Approximate solution at x = " + x + " is " + y);
   }
   
   public static void main(String args[]) throws IOException
   {
       EulerMethod obj = new EulerMethod();
       // Initial Values (Subject to change based on the problem)
       double x0 = 0;
       double y0 = 7;
       double h = 0.001;

       // Value of x at which we need approximation (subject to change based on the problem)
       double x = 1;

       obj.euler(x0, y0, h, x);
   }
}  return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```


