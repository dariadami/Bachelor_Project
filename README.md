# Blackbox

Source code from:
https://github.com/CSAILVision/gandissect

Download anaconda from: 
https://www.anaconda.com/download#downloads

Find the anaconda3-folder on your computer, and possibly add the path to the 'condabin' to PATH in system variables?
Not sure if needed.

In Vscode, open a WSL/Ubuntu terminal. Navigate to gandissect/gandissect-master folder.
Run: script/setup_env.sh
All uses of 'conda' are changed to 'conda.exe' in the script, so should work.
But you'll get an error: "PackagesNotFoundError: The following packages are not available from current channels:"
I tried to just manually download the missing packages but then ran into problems about dependencies and outdated packages :L
