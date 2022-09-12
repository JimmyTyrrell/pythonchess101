# pythonchess101
a simple OOP chess game in Python

It will need a turn sequencer to keep track of whose turn it is.
	At the beginning of each turn:
		current_turn	>= 1
		current_move_white = None
		current_move_black	= None
	When one side makes a move, it will make an input to their side's current_move variable.
	When both sides have finished their move, the inputs will be passed to the log, the turn counter will be advanced, and the variables will be defaulted to None for the next move.
	
It will need a log to keep track of the game.
	The 0 index of the log will point to an entry in a catalog of preset openings. 
	This will determine the opening layout of the board, populate the list with an appropriate set of preceding moves, and advance the turn counter to the current move. 
	The default value for this index will open the game with the standard opening setup, and no moves in the log.	
	Each set of values passed to the log will consist of: [current_turn, current_move_white, current_move_black]
	If the set includes a checkmate by white, then a None value will be passed to current_move_black
	
It will need a tiered set of rules to handle the movements of the pieces.
It will need a means of keeping track of which pieces are still in the game.
It will need a means of determining when a checkmate or stalemate has occured, and thus of ending the game.



It may include an in-game scoring system to keep track of which side is ahead on material.
It may include a rating system where players can keep track of their chess rating.
It may include onboard alerts showing the player when there is a dangerous situation for their pieces (en garde, forks, skewers, discoveries, etc)

turn sequencer = 
piece = parent class
	point_value
	position
	can_move boolean: checks if the turn sequencer allows it to move
	is_legal boolean: checks if attempted move is legal

pawn = child of piece
	point value = 1
	hasmoved boolean: checks if piece has moved yet
	secondmove boolean: checks if piece has made a second move
