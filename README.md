# Quizgame

live link: 
https://abhishek12071.github.io/Quizgame/

HTML Structure:
The HTML structure consists of a container element with a title and three main sections: game container, correct page, and wrong page.
The game container contains the options, input containers, and check/reset buttons.
The correct page and wrong page are initially hidden and are displayed based on the user's answer.

CSS Styling:
The CSS styling is responsible for the overall appearance of the quiz game.
It sets the background color, font styles, layout, and colors for various elements such as the cards, buttons, options, inputs, etc.

JavaScript Functionality:
The JavaScript code adds interactive functionality to the quiz game, including drag and drop for options and inputs.The components used are:

allowDrop(event): This function is responsible for allowing the drop event during drag and drop operations. It prevents the default behavior of the browser.

drag(event): This function is triggered when an option is being dragged. It sets the draggedOption variable to the current target element.

drop(event): This function handles the drop event when an option is dropped into an input container. It appends the dragged option to the target container. If the target container is an option, it appends the option to its parent container. It also checks if all inputs are filled and enables the check button accordingly.

checkResult(): This function is called when the user clicks the check button. It retrieves the values from the input containers and compares them with the correct sorted values. If the user's sorting is correct, it calls the showCorrectPage() function; otherwise, it calls the showWrongPage() function.

showCorrectPage(): This function hides the game container and displays the correct page, indicating that the user's answer is correct.

showWrongPage(): This function hides the game container and displays the wrong page, indicating that the user's answer is incorrect.

resetGame(): This function resets the game to its initial state. It clears the options and input containers, generates new random values, and enables the check button.

getRandomValue(): This function generates a random number between 1 and 1000 for the options.


Overall Flow:
On game load, resetGame sets up the initial state. Users drag options to input containers. Drop appends options. The check button is enabled when all containers have options. Clicking check triggers checkResult, displaying correct or wrong pages. Correct page shows congratulatory message and play again button, while wrong page shows error message and try again button. Clicking play again or try again invokes resetGame, resetting the game.
