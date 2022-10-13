# checkhdr: Gabe's HDR Checking Script
A simple(ish) script to check if the video in question contains the metadata for HDR playback.

## Dependencies
It is CRITICAL that your system have the ``ffmpeg`` package installed. Since this script is designed for macOS, you can install it via homebrew by running ``brew install ffmpeg`` in your terminal app of choice. If you're running this on a linux-based system, then you can just use your favourite package manager to install ffmpeg.

## Instructions
There are two ways to run this script. You can either run it in any folder on your disk by typing ``bash /path/to/checkhdr /path/to/filename.***`` or by adding the executable to your PATH. 

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



