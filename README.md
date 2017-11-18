# Author: Ping-Jung Liu
# Date: November 15th 2017
# COSC 76 Assignment : Motion Planning
# Acknowledgement: Professor Devin Balkom for providing the general structure 

***README***

importent files in this directory:

- prm_map.py

- prm_problem.py

- rrt_planner.py

- astar_search.py

- cs1lib.py

- display_planar.py

- planarsim.py

- SearchSolution.py

##########################################################
To test PRM planner with robot arm!!!
##########################################################
- open prm_problem.py and run directly with the default settings 
  of generate size 1000 and 15 neighbors

- to modify generate size and neighbors, open prm_map.py 
  they are at line 24 and line 26 respectively

- if you wish to test other map configurations, go to line 66 of prm_problem.py
  the main function

- prm_map takes in (width of map, height of map, list of obstacles, 
	                number of arms, lenghts of arms, resolution of collision check)
- prm_problem takes in (a prm_map, start configuration, goal configuration)

  configurates are lists of thetas, ex: (pi, 0, pi, 1.5*pi)

- use the following command to solve prm_problem
  result = astar_search(test_prm_problem, test_prm_problem.heuristics)

##########################################################
To test RRT planner with robot car!!!
##########################################################
- open rrt_planner.py and run directly with the default settings

- if you wish to change the terminate distance between config and goal,
  go to rrt_planner.py line 43

- if you wish to test other map configurations, go to line 163 of rrt_planner.py
  the main function

- rrt_planner takes in (width of map, height of map, obstacles, start, goal,
	                    delta(timestep), resolution)

- use the following command to solve rrt_planner
  solution = test_rrt.solve()
