
# CS 182: Artificial Intelligence
# Assignment 4: Markov Decision Processes and Reinforcement Learning
* Fall 2015
* Due: **Monday**, November 2, 11:59pm

In this assignment, you will implement sequence decision making algorithms and apply these to a gridworld and to Pacman. Note: We will use the Pacman framework developed at Berkeley. This framework is used worldwide to teach AI, therefore it is very important that you DO NOT publish your solutions online.









## Computational Assignment

### Question 1

Follow the instructions at:

http://ai.berkeley.edu/reinforcement.html

The page includes questions requiring implementation of sequential decision making and reinforcement algorithms we studied in class. [The grading scheme described on the Berkley webpage will not be used, but can be used for your own testing for evaluating your performance.]

For this assignment you are only required to do **Questions 1-7**. Question 8 is quite interesting though, so we recommend it if you have time and are interested in machine learning.

To get the assignment we recommend just cloning this repo:

> git clone https://github.com/CS182/HW4.git

 Solutions should be submitted to the course dropbox folder. Submit only the files `qlearningAgents.py`, `valueIterationAgents.py`,  and `analysis.py`. If you work in a pair, only one student should submit the files, but make sure to include the names of both students at the top of each of the files.


### Notes:

The framework for MDPs and reinforcement learning in this assignment is the same as the one discussed in class. However the reward specification is different than the one given in AIMA. While AIMA provides a helpful guide to this topic, if you want further notes on in the style of the assignment consult the text _Reinforcement Learning_ by Sutton & Barto available free at https://webdocs.cs.ualberta.ca/~sutton/book/ebook/the-book.html. 

## Written Assignment 

Answer the following questions individually, and submit as pdf to the dropbox folder. 

You control a solar-powered Mars rover. At any time, it can drive fast or slow. You get a reward for the distance travelled, so driving fast gives +10 (in all conditions) while driving slow gives +4 (in all conditions). However, if the rover shuts off, you will not get any reward no matter what you do. (It won’t move anyway...). Your rover can be in one of three conditions: cool, warm, or off. Driving fast tends to heat up the rover, while  driving slow tends to cool it down. If the rover overheats, it shuts off, forever. The transitions are shown in the table below. 


|Current condition | Fast or slow? |  Next condition |  Probability |
|------|-------|------|----------------------|
| cool | slow | cool | 1 |
|cool | fast | cool | 1/4| 
|cool | fast | warm | 3/4|
|warm | slow | cool | 1/4|
|warm | slow | warm | 3/4|
| warm | fast | warm | 7/8 |
| warm | fast | off | 1/8 |

### Question 1  

Model this problem as a Markov Decision Process: Formally specify the states, actions, transition 
function and reward function.

### Question 2

Write down the $U$ function for this problem in all possible states. Calculate by hand the values of $U$ assuming a policy $\pi_1$ when the rover always drives fast and $\pi_2$ when the rover  always drives slow.

### Question 3

Start with a policy where you drive fast no matter what the condition of the rover is. Simulate the first two  iterations of the *policy iteration* algorithm. Show how the policy evolves as you run the algorithm. What is the policy after the second iteration? For this question assume a discount factor of 0.9.


