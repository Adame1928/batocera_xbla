# XBLA-Automation 1.1

## Purpose:
### The purpose of this script is to extract, move, and organize all of your XBLA game archives for easy integration into EmulationStation in Batocera Linux

## Why it's necessary:
### The way that Xbox Live Arcade games were packaged was kind of weird. They were stored in a pirs container, which is like a weird archive format that only the xbox 360 used. In the past EmulationStation couldn't see these files because they dont actually have a file extension. Nopw we can trick it into seeing these files using a .xbox360 text file.

## How it works:
### The way the script works is by calling the patoolib module to extract the archives from the XBLA folder to the XBLA_Unpacked folder.
### It then renames the innermost file, the pirs file, to the name of the top level directory, which is your game name.
### Next it moves the newly renamed pirs file to the XBLA_Unpacked folder and deletes the original directory that the pirs file was in.
### Finally it creates the.xbox360 text file for each game and writes the game name into that file so that EmulationStation can see it.
### Now you should have a nice clean folder full of all of your XBLA games organized, named correctly, and without any unnecessary junk.
### The final step is all on you, it's time to move all of the game folders over to your Roms/xbox 360 folder in your EmulationStation DE directory.

Prerequisites:

Make sure you have a modern version of Python 3 installed, you can check this with python --version in the command line.
Make sure you have some kind of unarchiving program that can handle Rar files.

Instructions for use:

In the command line install patool using "pip install patool".

Download the zipped project file and extract all of its contents to your home directory.
In Windows this is usually C:\Users\username.
In Linux this is usually /home/username.

Place all of your archived XBLA games in the XBLA folder.
If the archive name doesn't match the title of the game then fix that now.

Open a command line in your home directory and run "python3 extract.py"
The program is now fully automated so you can just sit back and watch it work!

Now you can move all of the game folders over to your Roms/xbox 360 folder in your EmulationStation DE setup and run the scraper.