M1
I could have modularized my text editor by simply having a module for each feature.
Module 1: Input.  This module takes in the users keyboard inputs, determines if a shortcut or if the user is just typing and hands it over to the shortcut module if its a shortcut and hands it over to the editor module if the user is editing.
Module 2: Shortcuts.  This module takes in the shortcut input from the input module and decides what to do based on the shortcut.
Module 3: Editor.  This module takes what it is given by the input module and edits the file contents.
Module 4: File Handler.  This module views, updates, creates, and deletes files.  This module gives the contents of a file to the editor and takes new contents from the editor when saved.
Module 5: View.  This module handles all that the user sees.  It works with the file handler to know what files to show on the side bar, it works with the editor to know which text to show, and it works with the syntax highlighter to know what color to show the text.
Module 6: Syntax Highlighter.  Gets the contents of the file from the editor and decides what colors each character is then gives that information to the view.

M2
I modularized part of my text editor.  I separated the view from the actual file contents.
Module 1: View.  This module knew what part of the file the user was currently on and it only got that part of the file from the model.
Module 2: Model.  This module dealt with things like file structure, file contents, saving and loading files, and handling user input.
Module 3: MultiWindows.  This module handled the number of windows and which windows and tabs were linked to which files.  This module told the view abd the model which tab and window was currently selected.