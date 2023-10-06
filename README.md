# Console-Based Battleship Game (with Game History)

## Objective:
In this exercise, you are tasked with creating a simplified, console-based version of the classic game Battleship. Your implementation should be object-oriented and should keep a record of past games that persists across program runs. You can choose to implement this game in either Python or JavaScript.

## Specifications:

### Classes 
- **Game**: Manages the overall game logic.
- **Board**: Represents the game board.
- **Ship**: Represents a ship on the board.
- **Player**: Represents a player.
- **GameHistory**: Keeps track of past games.

### Game Play
- The board should be a 10x10 grid.
- Each player gets two ships: one of length 3 and one of length 4.
- Players take turns to attack a position on the opponent’s board.
- The game continues until all ships of a player are sunk.

### Game History
- After a game ends, save the game result (who won, number of moves, etc.) to a file.
- At the start of a new game, load the game history from the file and display it to the user.

### Persistence
- Use file handling to save and load game history.

### Console Interface
- Create a simple text-based interface for user input and game feedback.
- Each player should be prompted to enter their move during their turn.

### Error Handling
- Include appropriate error handling for invalid input and file operations.

## Additional Specifications:

### Ship Placement
- Each ship should occupy adjacent cells on the board either horizontally or vertically.
- Ships cannot overlap or be placed off the board.
- At the beginning of the game, players should be prompted to place their ships on the board. They should input the starting coordinate (e.g., A1) and orientation (horizontal or vertical) for each ship.
- Optionally, add a random placement feature where the game randomly places the player's ships on the board.

### Computer Player
- Create a **ComputerPlayer** class that extends the **Player** class with additional AI functionality for making moves.
- Implement a simple AI algorithm for the computer player to make moves. For example, a random guessing algorithm or a more sophisticated hunting/targeting algorithm.
- During the game, players should be able to choose to play against another human player or the computer player.

## Tips:

### Error Handling
- Make use of try-catch blocks (or try-except in Python) to handle potential exceptions, especially when dealing with file operations and user input.
- Provide clear error messages to inform the user about what went wrong and possibly how to fix it.
- Consider creating custom exception classes to handle game-specific errors.

### File Operations
- For saving and loading game history, consider using a format like JSON or XML as they are structured, human-readable, and easily parsed.
- Ensure file operations are handled in a way that does not disrupt the game, e.g., if the file cannot be written to or read from, the game should handle this gracefully.

### User Interface
- Keep the user interface simple and intuitive. Clear prompts and feedback will help users understand the game state and what actions they can take.
- Consider implementing a help command that explains the rules, how to input commands, and other useful information.

### Extensibility
- Design your classes and methods in a way that allows for easy extension or modification in the future. For example, making the AI strategy replaceable, or allowing for different board sizes and rules.

### Performance
- While this is a simple console game, always keep performance in mind, especially when dealing with loops and file operations.

### User Feedback
- Offer feedback on player actions, such as hits, misses, and sinking of ships. Clear feedback helps players understand the consequences of their actions and the current state of the game.

### Learning Resources
- If unfamiliar with certain concepts or technologies, don't hesitate to seek out tutorials, documentation, or forums for help. Continuous learning is a crucial part of software development.

### Ship Placement
- When prompting for ship placement, check the validity of the input for both coordinates and orientation.
- Check the selected board positions to ensure they are within bounds and not already occupied by another ship.
- Consider creating a method within the **Board** class to handle ship placement, which can be reused for both human and computer players.

### Computer Player
- You could start with a simple random guessing AI where the computer randomly selects a cell to attack. Ensure the same cell is not attacked more than once.
- For a more advanced AI, implement a hunting/targeting algorithm. In hunting mode, the AI randomly shoots at cells. Once a hit is made, the AI switches to targeting mode and attempts to sink the ship by attacking adjacent cells.
- Consider creating separate methods for the different AI strategies, which will help keep the code organized and make it easier to improve or change the AI behavior in the future.
   
- To ease the transition between human and computer players, ensure that the **Player** class has a consistent interface for making moves. This way, the **Game** class can interact with human and computer players in the same way, regardless of their type.

## Guidelines:
- Start by planning the classes and their relationships.
- Create a class diagram to visualize the structure of your program.
- Implement the classes one by one, testing each class as you go.
- Ensure the game flow works correctly and that game history is saved and loaded appropriately.
- Make sure your code is well-commented and follows the coding standards of the language you choose.

## Challenge:
- Extend the game to support more players and more ships.
- Implement additional features such as different types of ships (with different lengths and shapes), hidden mines, or power-ups.
- Enhance the console interface to make the game more interactive and user-friendly.

  Happy Coding!!
