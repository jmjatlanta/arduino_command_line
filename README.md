The goal of this little project is to work with boards like Arduino, but without the IDE. This will help me separate what is Arduino from what is the basic hardware.

This project uses the project from a9183756-gh called Arduino-CMake-Toolchain, which is a submodule of this project. Therefore, after `git clone https://github.com/jmjatlanta/arduino_command_line.git` you'll also need to `git submodule init`

CMake uses the idea of a board options file. There are several ways to specify this.
- From within the CMake GUI
- After the initial run, a file named "BoardOptions.cmake" is created, where you uncomment the board you are working with, and re-run cmake (this is the way I've been doing it so far).
- You can create your own arduino board options file and pass it to cmake with the `-DARDUINO_BARD_OPTIONS_FILE=<file>`
- You can programmatically "walk" the menu of the Arduino IDE on the command line like so: `-DARDUINO_<BOARD_ID>_MENU_<MENU_ID>_<MENU_OPT_ID>=<TRUE|FALSE>` (a bit difficult if you ask me)