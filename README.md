Methodology
The methodology of the Noughts and Crosses with Alpha-Beta Pruning project outlines the steps taken to implement an AI agent capable of playing the game optimally. Below are the key components:

1. Game Representation
Board State: The game board is represented as a list of 9 elements in Python, corresponding to the 3x3 grid of Noughts and Crosses (Tic-Tac-Toe). Each element can either be empty (' '), contain an 'X' (representing the AI player), or contain an 'O' (representing the human player).
Moves: Players (AI and human) take turns marking empty spaces on the board. The AI is designed to play optimally based on the current state of the game.
2. Minimax Algorithm
The Minimax algorithm is the core decision-making process of the AI:

The algorithm explores all possible moves and assigns a score to each potential outcome. The AI aims to maximize its score (as the maximizing player) while the opponent tries to minimize the AI’s score (as the minimizing player).
It operates in a recursive manner, simulating every possible move and evaluating the end state (win, loss, or draw).
Evaluation Function:
The board state is evaluated based on the win/lose/draw conditions.
A score of 1 is returned if the AI wins (with 'X').
A score of -1 is returned if the opponent wins (with 'O').
A score of 0 is returned if the game is a draw or ongoing.
3. Alpha-Beta Pruning
Alpha-Beta Pruning is an optimization technique used to enhance the efficiency of the Minimax algorithm:

Alpha represents the best value found so far for the maximizing player (AI).
Beta represents the best value found so far for the minimizing player (opponent).
If a node’s value is worse than the current alpha or beta, the algorithm will stop exploring that branch (i.e., prune it), thus reducing the number of moves that need to be evaluated.
This significantly speeds up the decision-making process by eliminating unnecessary calculations.
4. Game Logic and Turn-Based Decisions
The AI is implemented to make its move first (as the maximizing player) and the human player moves afterward (as the minimizing player).
The algorithm repeatedly evaluates all possible moves for the AI's turn, selects the best move, and updates the board.
For each move, the algorithm uses the Minimax function to recursively explore all possible game states and returns the optimal move.
5. End Condition and Result Evaluation
The game continues until a player wins or the board is full (draw).
The AI checks the result after each move (for both the AI and the human player) and announces the outcome accordingly.
