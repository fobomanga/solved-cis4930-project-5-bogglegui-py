Download Link: https://assignmentchef.com/product/solved-cis4930-project-5-boggle_gui-py
<br>
<h1>1           boggle_gui.py</h1>

In this final assignment, we will be revisiting the first module we put together this semester: boggle.py. This time, you need to extend your module to add the following features:




<ul>

 <li></li>

 <li>Saving/loading games.</li>

</ul>




All of the game requirements of the first assignment hold (e.g. grid must be 4×4, dice must be randomly shuffled, same game rules and scoring apply, etc).  You may repurpose your original boggle.py module for this project, but you will likely need to make significant structural changes so it may be best to start fresh and add in previously-used code bits as necessary. You will likely need to use a few of the things we’ve discussed this semester, including standard library modules like random, data persistence modules like sqlite3 or shelve, as well as, of course, a GUI toolkit (PyQt5). Please feel free to be creative with the look and feel of the application and search for creative, pythonic solutions to the challenges you encounter (including revisiting your original boggle.py code – look for ways to make it better!).




<h2>GUI</h2>

You may structure your GUI however you’d like as far as aesthetics and layout go. The following must be present, however:




<ul>

 <li>A descriptive window title (e.g. “Play Boggle!”).</li>

 <li>The dice grid: a 4×4 display of the 16 die faces in which the user looks for words.</li>

</ul>

Suggested widgets: QtWidgets.QLabel. Hint: notice that it inherits from QFrame, which has styling     options.

<ul>

 <li>A text box displaying a list of words already entered.</li>

</ul>

Suggested widget: QtWidgets.QTextEdit.

<ul>

 <li>A line editing field for submitting words. Pressing enter in this field should add the word to the text box. Suggested widget: QtWidgets.QLineEdit.</li>

 <li>A button to start the scoring process. Clicking this button should end the game and start the scoring process.</li>

</ul>

Suggested widgets: QtWidgets.QPushButton

<ul>

 <li>A Game menu with options to start a new game, save a current game, or load an existing game.</li>

</ul>

<h2>Ending the Game</h2>




When the game is ended by the user, a window should pop up (suggestion: QMessageBox), telling the user what their score is (no details required) and asking them if they’d like to play again. The default option should be “Yes”. If they select to play again, all text should be cleared and the dice shuffled. If they select no, the application should close.




<h2>Saving and Loading Games</h2>

<strong> </strong>

You will need to allow users to both save and load games. Saving and loading a game means:




<ol>

 <li>Saving and restoring the dice configuration.</li>

 <li>Saving and restoring the words already entered (i.e. the ones in the right text box).</li>

</ol>




Saving and loading should work between application instances so you will need to use some persistent storage scheme (e.g. file data, sqlite database, shelve, etc). The choice of scheme is up to you – please just be sure to include any supplementary files if necessary (an sqlite file, for example).




Saving can be performed by selecting the Save action from the Game menu in the menu bar. When the user selects the Save action, the current state of the game should be recorded and saved, but the user will not see any further action take place. Saved games will be identifiable by a time stamp indicating when the game was saved.




Loading can be performed by choosing the Load action from the Game menu in the menu bar.










In this case, a dialog box should pop up (suggestion: QDialog and QListWidget may be of use here) listing the saved games available, identifiable by the time and date that they were saved. The saved games should be ordered, with the most recent game appearing first.  The game which is selected by the user (by clicking on the saved game), should replace the current state of the game in the main window. <strong> </strong>

<strong> </strong>

<strong> </strong>







You are free to use whichever modules you’d like for this assignment as long as they are from the standard library or PyPI. If you find a module or code from elsewhere that you would like to use, you should come talk to me first. Your GUI can be in any style or layout you’d like as long as it has the required components.




<strong>In summary, I will be looking for the following requirements to be met while grading:</strong>  – Boggle game logic and scoring is correct.

<ul>

 <li>5 listed GUI components (dice grid, word list, word input box, score button, and Game menu) are present and functional. You may add more if you’d like.</li>

 <li>User is allowed to start new game or load a saved game.</li>

 <li>User can end the game by pressing the right-hand side push button, displaying a pop up box with the score. The user should be allowed to quit the application or continue with a new game.</li>

 <li>User can opt to start a new game, save a current game, or load a saved game through the Game menu.</li>

 <li>When the user loads a new game, they can select from a list of saved games. Saved games are identified and ordered by the time and date they were saved.</li>

</ul>

<strong> </strong>