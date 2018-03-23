# NIM_game
Machine learning used to develop an unbeatable player of "NIM game" programmed in Python

See definition of the NIM game under https://en.wikipedia.org/wiki/Nim

The program has a dumb terminal interface with minimal graphics that lets you do the following 
- (R)ules: displays game rules 
- (P)lay: you can play against the computer 
- (L)earn more: runs ML (reinforcement learning) to develop game playing skills 
- (S)how my knowledge: shows the knowledge base of the computer 
- (E)xit: exits the program

When in learning mode the program generates two instances of a player and they start playing games against each other. 
In the beginning both players select their moves randomly but after each game the possible moves are marked as follows:

- all possible gameboard arrangements or positions (number of stones in each heap) correspond to a matrix element
- the matrix (multi-dimensional array) holds the values of the positions
- the higher the value the more likely is that the position is good (probably a winning position)
- the value of the positions that were used by the winner are increased by 1
- the value of the positions that were used by the looser are decreased by 1 

The values are used to improve the selection of the next move by each player while learning. The position having the higest value is selected from the available possible ones. If more than one position have the same highest value a random choice is made among them. By applying this method the program slowly finds the winning positions after a couple of thousand games. These winning positions form the winning strategy.

Interesting observations:
- sometimes "wrong" positions are identified initially as winning positions but the program forgets these positions (decreases their value) after more learning iterations
- the program converges to the winning positions
- convergence is achieved (meaning the winning positions are found) even if we change the size or number of heaps.

Have fun! 

Gabor
