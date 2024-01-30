# Blackbox

Source code from:
https://github.com/CSAILVision/gandissect

Download anaconda from: 
https://www.anaconda.com/download#downloads

/*
The setup_env.sh script just straight up does not work for me. It always freezes when trying to set up the environment. I had to manually download create the environment, then install the packages one by one.
*/

Find the anaconda3-folder on your computer, and add the path to the 'condabin' to PATH in system variables.

Open the Anaconda Navigator, and launch 'CMD.exe Prompt'. This will open a terminal, where you must run this command:
    conda init

You can now close that terminal and Anaconda Navigator.
Open the project in your IDE, and open a terminal (command prompt? powershell?).**
Run the following command to create an environment (named netd) in anaconda:
    conda create --name netd

Enter environment: 
    conda activate netd

Manually install all packages in environment.yml (dont worry about the 'channels')
Example:
    conda install python=3.11

Then run the rest of the setup-scripts (possibly not download_data??**)
I encounter problems when trying to dissect a GAN using: python -m netdissect ....


OUTDATED - DONT DELETE:
In Vscode, open a WSL/Ubuntu terminal. Navigate to gandissect/gandissect-master folder.
Run: script/setup_env.sh
All uses of 'conda' are changed to 'conda.exe' in the script, so should work.
But you'll get an error: "PackagesNotFoundError: The following packages are not available from current channels:"
I tried to just manually download the missing packages but then ran into problems about dependencies and outdated packages :L