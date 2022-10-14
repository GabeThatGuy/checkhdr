# CheckHDR: Gabe's HDR Checking Script
A simple(ish) script to check if the video in question contains the metadata for HDR playback.

## Dependencies
It is CRITICAL that your system have the ``ffmpeg`` package installed. Since this script is designed for macOS, you can install it via homebrew by running ``brew install ffmpeg`` in your terminal app of choice. If you're running this on a linux-based system, then you can just use your favourite package manager to install ffmpeg.

### THIS SCRIPT WILL NOT WORK OR RUN ON WINDOWS SYSTEMS

## Todo
This repo has a todo list. Click the projects tab above (or click [here](https://github.com/users/GabeThatGuy/projects/1)) to view it.
## Instructions
There are two ways to run this script. You can either run it in any folder on your disk by typing ``bash /path/to/checkhdr /path/to/filename.***`` or by adding the executable to your PATH. If the executable is in your path, you can run the script anywhere by typing ``checkhdr filename.***``

> Note: Bash scripts are very temperamental when it comes to storing paths in variables, so it's recommended you add the script to your PATH and navigate to the directory containing the file in question before running the script to avoid entering any paths into the command. 

### Adding the script to your PATH.
I'm going to assume you've never added a folder to your PATH before. If you have, just add the script executable into a folder that's already in your PATH.
Steps:
1. Open terminal
2. Type ``cd ~`` - This will change your working directory to your home folder.
3. Type ``mkdir Scripts`` - This will make a folder in your home folder called Scripts. This is where we will put the checkhdr executable.
4. Leave the terminal window open. Open your file explorer and navigate to ~/Scripts.
5. Copy the checkhdr executable from your downloads folder into the Scripts folder.
6. Switch back to the terminal window and type ``sudo chmod 755 checkhdr``. This will give your user permissions to run the executable, if they were not already granted.

That's it! You're now ready to use checkhdr anywhere on your system.
> Note: It's possible that your shell won't recognize the executable until you quit and reopen your terminal app, so if you run the script and it says "command not found" or something like that, just quite and reopen.

## Expected Output
This script will have many different outputs:
#### Output 1: Video is HDR, and encoded in HLG or Dolby Vision
If this is the case you will get the following output in your terminal:  
``Target video [filename] is HDR and encoded in [HLG / Dolby Vision]``

#### Output 2: Video is HDR, and encoded in PQ
If this is the case, you will get the following output in your terminal:  
``Target video [filename] is HDR and encoded in [PQ]``

#### Output 3: Video is SDR
If this is the case, you will get the following output in your terminal:  
``Target video [filename] is SDR.``

#### Output 4: Couldn't fild file
If this is the case, you will get the following output in your terminal and the script will exit prematurely:  
``[CRITICAL] Could not find file name.ext in /path/to/currentDirectory``



## Troubleshooting
### Recommended Toubleshooting Steps
1. Check that your file exists in the directory you're running the script from.
2. Check that you included the file extension when running the script.

If you've tried and ensured that your filename and working directory are correct, have a look at the to-do section as well as the issues tab to see if the problem you're having was already reported or is being worked on. If not, go ahead and open up an issue report in the issues tab. 
