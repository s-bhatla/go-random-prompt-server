# Go Random Prompt server

Code for solving an issue I encountered while creating a StoryChain online game. Each player would write a random story prompt, and the prompts would be randomly distributed among all the players in the room. The prompts should not repeat for one player unless all the other players have received a prompt from all other players. The game will end when the set number of rounds are complete.

Let us take an example of 5 players:

`{"A", "B", "C", "D", "E"}`

`
matrix := [][]string{
		{"A", "C"},
		{"B", "A"},
		{"C", "B"},
		{"D", "E"},
		{"E", "D"},
	}
`

 The algorithm needs to successfully find the third column in the matrix, one in which all elements will be unique for both row and column. 
 The proposed most effective solution is similar to the 'Sudoku Solver', employing backtracking techniques. An additional slice randomizer is added so the results are random and still satisfy the required conditions.

 Output:
 
 `New column can be :  [B E D C A]`
