---
layout: project
type: project
image: images/sudoku.jpeg
title: Sudoku
permalink: projects/sudoku
# All dates must be YYYY-MM-DD format!
date: 2021-10-01
labels:
  - Java
  
summary: A bruteforce recursive program to solve a sudoku puzzle (ICS 211).
---

<img class="ui medium right floated rounded image" src="../images/Screen Shot 2022-01-19 at 10.37.25 PM.png">

This sudoku project was an assignment solved in ICS 211. In this project we learned and practiced recursion in a brute force approach to solve a few sudoku puzzles using Java in the Elcipes IDE. In this project we also recorded the runtimes of each of the three different puzzles and analyzed them. 

Example 3 the AI Escargot of this project, takes significantly longer to complete. While the other 2 examples took less than a hundredth of a second, the last one took more than a hundredth of a second. Looking at Example three there are significantly more empty blocks and therefore more possible legal values. Since the algorithm uses backtracking to rule out values, it will take longer. If that legal value doesn’t work, it will return to that point, and try a different value, until all the available values have been tried.

The best case scenario would be if it finds all the valid numbers on the first run. The worst case would be that every single cell is incorrect and does not have a solution at the end. The main dilemma with AI Escargot is that it would have to backtrack more, taking up more time. This means that this particular example is closer to the worst case scenario because it has a higher chance of being incorrect.

I admittedly found this project gruelling and long but it helped me strengthen my understanding of recursion and the importance of program and algorithm analysis on a beginner conceptual level. 
 
Source: <a href = "https://github.com/mahi3crab/Sudoku"><i class="large github icon"></i>mahi3crab/Sudoku</a>.
