board = []

# Populate the board with "O"
for item in range(5):
  board.append(["O"] * 5)

# Align the board into a grid formation 
# Join the rows to make it look nicer
def print_board(board_in):
  for row in board_in:
    print " ".join(row)


# Randomly determine the placement of the ships
def random_row(board_in):
  location = randint(0, len(board_in) - 1)
  return location

def random_col(board_in):
  location = randint(0, len(board_in) - 1)
  return location

random_row(board)
random_col(board)

# Allow the user to input their guesses
for turn in range(4):
  guess_row = int(raw_input("Guess Row: "))
  guess_col = int(raw_input("Guess Col: "))
  if guess_row == ship_row and guess_col == ship_col:
    print "Congratulations! You sunk my battleship!"
    break
  else:
    if (guess_row < 0 or guess_row > 4) or (guess_col < 0 or guess_col > 4):
      print "Oops, that's not even in the ocean."
    elif(board[guess_row][guess_col] == "X"):
      print "You guessed that one already."
    else:
      print "You missed my battleship!"
      board[guess_row][guess_col] = "X"
  print "Turn", turn + 1
  if turn == 3:
    print "Game Over"

  print_board(board)
