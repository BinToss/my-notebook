Invader script comments
if the game engine can handle it improve Invader by retaining comments in Scripts after they've been compiled
Add a command line switch to toggle the option to embed commented-scripts or to strip comments upon map compile.
if the game engine cannot handle commented scripts, then strip the comments and add a commented copy of the script as a dummy tag to retain the comments
This will create one tag for scripts that will allow the scripts to be used in game and another that is there only to keep comments in but will not function in game