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

UPDATE 28/01/2024:
The setup_env.sh script just straight up does not work for me. It always freezes when trying to set up the environment. I had to manually download create the environment, then install the packages one by one.
I did this in command prompt.
Create environment: conda create --name netd

Enter environment: conda activate netd

Manually install all packages in environment.yml (dont worry about the 'channels')
Example:
conda install python=3.11

Then run the rest of the setup-scripts.
I encounter problems when trying to dissect a GAN using: python -m netdissect ....

