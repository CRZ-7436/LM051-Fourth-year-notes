<span style="color:#00b050">Notes:</span>

<span style="color:#7030a0">ResNet</span>
	top 5 error rate of 3.6%
	DNN with 152 layers
	Uses idea of skip connections
		to avoid the problems of vanishing graients
		to mitigate the degradation(accuracy saturation) problem
		- adding more layers to a suitably deep model leads to higher training error.
	input into a layer is also added to the output of a layer higher up layer in the stack

<span style="color:#7030a0">GoogleLeNet</span>
	winner of 22014 ISLRVC
	top 5 error less that %
	much deeper than previous CNNs
	fewer parameters 6 million instead of 60 in alex net

<span style="color:#7030a0">Reinforcement learning</span>
	objectives
		Outline the motivation for RL
		describe the challenge
		Characterise RL as an MDP
		Enumerate the RL components
	JJ beats children "no point having a conversation with an 18 month old"
	Motivation: use case
		learning to play checkers/Connect4/chess/backgammon/go.....
		knowing the rules is not sufficient to be competitive
		solution: Reinforcement learning
		RL -> learning by trial and error
		learn -> optimal mapping from states to actions
		state -> board configuration
		connect 4: 10^12 states
		actions -> permissible actions allowed for a particular state
		maximising long term REWARD
		reward for a game: +1 for a win, 0 for a loss