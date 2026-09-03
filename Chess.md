* Goal: Make the strongest chess bot possible within the 50 MB limit.
* Minimal architecture chosen: Alpha-beta minimax + neural-network evaluation.
* Simpler alternative: Your current negamax is already minimax-equivalent and easier to implement.
* Alpha-beta: Same result as minimax, but prunes branches that cannot affect the decision, making search much faster.
* Neural-net evaluation: Give the board position to a trained NN that outputs a score representing how favourable the position is.
* Current code: Has negamax/minimax, but does not have alpha-beta pruning yet.
* Best practical plan: Start with your current negamax → add alpha-beta → add a small chess-specific NN evaluator.