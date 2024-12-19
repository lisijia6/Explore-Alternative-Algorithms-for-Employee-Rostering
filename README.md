# Optimize-Coverage-for-Employee-Rostering-Problem

This is the code base for a data science (optimization) project: Optimize Coverage for Employee Rostering Problem.

## Introduction
Ceridian (the client) is a global human capital management (HCM) software company that provides work intelligence solutions and services for all kinds of organizations. It currently uses a modification of Greedy Randomized Adaptive Search Procedure (GRASP) metaheuris- tics to solve employee rostering problems. The current algorithm is capable of generating feasible schedules, but it has no guarantee of solution quality. Therefore, the client is look- ing to explore alternative algorithms that can either outperform GRASP in solution quality within a reasonable amount of time or be embedded to help improve GRASP (the baseline).

The goal of the project is to explore, research, and develop a rostering algorithm that is able to give a better solution quality. The ideal output should be a roster developed over a 7-day planning horizon, based on employee availabilities, employee skill sets, appropriate shift lengths, number of consecutive work days, and so forth.

While performing the literature review, the capstone team explored a variety of method- ologies used to solve rostering problems, such as mathematical programming, constraint programming, and multi-agent approaches. One or a combination of these methodologies may be adapted and incorporated into the design of new employee rostering algorithm(s).

An integer programming (IP) model is formulated to create seven-day rostering schedules. The model aims to minimize the demand coverage penalty (from overstaffing and under- staffing) while enforcing a set of selected fundamental scheduling constraints, such as mini- mum time between shifts and maximum daily hours.

Two synthetic local diner datasets and one real cosmetics store dataset are used to generate rostering schedules and evaluate the IP model. Compared to the baseline model (GRASP), the IP model outperforms GRASP in terms of roster quality, guaranteeing optimal rosters created. Although similar performances are achieved on smaller problem instances in terms of computational speed for both GRASP and IP model, GRASP outperforms the IP model for larger problem instances. This makes sense as GRASP is a heuristic algorithm that searches for a local optimal value in a small neighbourhood, whereas the IP model has a much larger search space and finds a global optimal value.

In conclusion, the IP model does not outperform GRASP completely. The capstone team recommends leveraging the IP model for smaller problem instances and GRASP for larger and more complex problem instances. Therefore, decision makers have to make a trade-off between solution quality and computational speed depending on problem sizes.

## Usage
Code and toy examples are contained in ./results directory (i.e., data, LP specification, ipynb notebook). Run the ipynb notebook within each toy example to reproduce the results. 

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute the code according to the terms specified in the license.