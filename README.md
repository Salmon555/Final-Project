# 590PR Final_Project

# Each teammates' commitment
### Xianzhuo Cao: Choosing the code and understanding it thoroughly, then make some improvements in the algorithm and the code. Coding in the simulation part.  
### Xiaoxin Wang: Comimg up with the idea fo Gomoku. Searching for appropriate algorithm and code for the simulation. Coding in the simulation part.
### Wendi Zhang:  Searching for the appropriate algorithm and code, do the testing for the code and the simulation. Making the powerpoint for the presentation.

# Explanation for all files in github
### Monte Carlo.ppt: This is the powerpoint for the presentation.
### play_with_AI.py : This is the python program in which you can play with a AI with tree depth of 3
### graphics.py: This is a py file which provide graphics and source of user interfaces. This is a copy of other's code
### simulation.py: This is the py file for Monte Carlo simulation. The program simulating 100 games a time using 2 AIs.
### simulation_final_version: Final version of our simulation (inlcude 5-in-a-row and 4-in-a-row determined by parameter success_num)
### result.txt: Result so far
### Result Analysis.pdf: the Result analysis according to the test result of 5 stone rule and 4 stone rule for 7 different first move

# Title: A Chess Game: Gomoku(Five in a row)

## Team Member(s): Xianzhuo Cao, Xiaoxin Wang, Wendi Zhang


# Monte Carlo Simulation Scenario & Purpose: 
### We will redesign an AI for the game using Python. Then two AI will simulating the game thousands of times.


## Simulation's variables of uncertainty
### Different first move, Different AI, Additional rules 

## Hypothesis or hypotheses before running the simulation:
### The best first move might be placing stone in the center. 
### The further your first move away from the center, the less winning rate you will get.

## Our experiment:
### Due to the time complexity, we tested 7 different first move for 2 different rules of 4-in-a-row and 5-in-a-row, each move has 1000 games played by 2 AIs.

## Analytical Summary of your findings: (e.g. Did you adjust the scenario based on previous simulation outcomes?  What are the management decisions one could make from your simulation's output, etc.)
### The best first move should is in the center, and the difference between center and 1 step from it is not obvious due to the large board.
### The first one to move has great advantage in this game.
### According to the result, we may sketchily draw the conclusion that the further your first move away from the center, the less winning rate you will get
### If we change the rule to four in a row to win, the first one to move will always win.
### If we change the rule to six in a row to win, this game will hardly end and there will be tie for almost every game.
### We can only do the Monte Carlo Simulation in the tree depth of 1 due to the high time complexity, the disadvantage of this is that the AI is too stupid.
### If we can set up the tree depth to 3, or even 5. The AI will be very smart and the result will be more convincing.
### We tried to apply numba to accelerate the program. It turned out that numba is not approriate in most of our function and will increase the running time. However, I tried to apply it in function call game_win, this will decrease the running time of 10 games from 22.19 to 19.98 by taking the average of ten attempts.

## Instructions on how to use the program:
### Run play_with_AI.py to play the game of Gomoku 
### Run simulation.py to simulate the game 100 times

## All Sources Used:
### https://github.com/colingogogo/gobang_AI 
### And some website explaining the algorithm of game tree and prunning.

# Run the code
### 1.Change the amount of simulation time:line 482. Because of its complexity, to get a 1000 times simulation result, we run it 100 times each time. For 5-in-a-row, a laptop with intel core5 spends around 7 minutes to do 100 times simulaiton.And for 4-in-a-row, a laptop with intel core5 spends less than 1 minutes to do 100 times simulaiton.
### 2.Change the rule(4-in-a-row or 5-in-a-row):line 483.
### 3.Change the start position:line 15. To change the start position from (1,7) to (7,7)
