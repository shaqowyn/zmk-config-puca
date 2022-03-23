
# Puca-Macropad-ZMK

A wireless firmware based on zmk for the Puca Macropad by ffkeebs.


## Author(s)

- [@AXRAY23](https://www.github.com/AXRAY23) - puca implementation
- [@zmkfirmware](https://www.github.com/zmkfirmware) - firmware

## Thanks to:

- zmk discord community for help in building the firmware
- mechwild for the murphpad implementation from where i've taken some code snippets

## Usage

If you're like me, i.e you have no experience with Github, ZMK or coding but still want to make your pucapad wireless using a nice! nano with ZMK, hopefully the following steps will help you understand what you to need to do.

```
This repo is a fork of the zmk-config-puca repo created by AXRAY23. 
At the time of writing there is only a verified ZMK firmware available for the ffkeebs Murphpad but not the 
Puca. Thus, your only options are to either code a new shield for the Puca from scratch using ZMK, 
imo unrealistic to do this unless you want to learn or already know how to do so efficiently or make a fork 
of AXRAY23's repository like I did and adapt the keymap files to the way that you want it.

I found it pretty difficult as a beginner to understand the steps I had to take so hopefully this helps:

Step 1: make a GitHub account

Step 2: go to AXRAY23's repo for the puca -> https://github.com/AXRAY23/zmk-config-puca

Step 3: at the upper right corner of the repo, click fork which will create a clone of the repo 
in your GitHub account. The clone is yours and thus gives you the ability to play around with the 
files and modify them as you see fit without destroying the work of AXRAY23.

There are multiple ways to approach the remaining steps, I'll tell you how I did it in Step 4 to 14.
My way teaches you more about GitHub, editing files offline and incorporates the use of a text
editor. If you want my more complicated but more useful in the long term way,
skip the paragraph below and go on to step 4.

However, there is an even easier way. That'll I'll explain now.

Basically, fork AXRAY23's repo (Step 1 to 3). Then on the <> Code tab go into the config folder.
Click the .keymap files and open it, click the pencil (edit button) in the taskbar. 
This will let you edit the keymap straight away on GitHub, how-to code the keymap is in Step 9 below.
After you're done editing commit it to you're forked repo at the buttom of the page and you're done!
You can get your newly built firmware from the actions tab (step 12).
Install it to your Puca (step 13 - 14).

Step 4: download the GitHub Desktop app and set it up to be linked to your GitHub account online. 
The desktop app will make pushing your updated .keymap and .conf files to your remote 
repository on GitHub very easy. You need to do this last step because the firmware gets built on GitHub.

Step 5: clone the files from the forked repo to your PC. Easiest way to do this: on the <>code tab 
of the repo, click on the code button and choose download zip from the dropdown list.

Save the download to your desired location on your PC and unzip. 
You should find a folder called zmk-config-puca.

Step 6: open the Github Desktop app, click on "add a local repository" and 
select the folder you cloned to your pc -> zmk-config-puca

Step 7: this step is not mandatory but I think it makes editing the files in the folder easier. 
Download a nice text editor like VScode, Pycharm or Sublime Text. 
For the rest of this example I use VScode.

Step 8: Open VScode, navigate to the zmk-config-puca folder in your directory. Go into the config folder. 
You'll need two files primarily: puca.keymap and puca.conf. puca.keymap is where you'll change the keymap 
to have your desired key bindings. puca.conf is where you can enable or disable the additional hardware 
features of the puca like the OLED, rotary encoder, underglow LEDs etc. depending on your needs. 
For the .conf file all you need to do is comment a existing code line to disable it 
or uncomment it to enable it. 
Placing a # infront of a line of code makes it a comment i.e. it would not be read and run as code, 
removing # uncomments it!

Step 9: onto the keymap. Open the puca.keymap and start editing the keymap as is needed for your purposes. 
This link: https://zmk.dev/docs/features/keymaps will explain the basics to you, it's not hard.
Esentially you'll be customizing the keycap using specific key codes that ZMK recognizes. 
All the key codes can be found here: https://zmk.dev/docs/codes/, use ctrl + f to find what you need quicker. 
Save the file when you're done.

Step 10: once you've saved your updated keymap, the GitHub desktop app should immediately notice that 
you have made changes to a file in the local zmk-config-puca folder on your PC. In the right bottom of the 
screen it will present you the option to commit the changes. Commit the changes and use the comment section 
above the commit button to make a note for yourself what changes you made e.g. "new keymap for gamepad layer". 
This is useful the more commits you run because at some point you won't know which changes are which anymore.

Step 11: on the next page after you commit, push the commited changes to your online aka remote repository 
on your GitHub account by selecting the push option.
Once you've done this the changes will become visible on GitHub, you probably have to refresh the webpage. 
Under the actions tab in the remote repository you will realize that GitHub automatically runs the workflow 
script to generate a new build with the changes you've made. You're basically almost done at this point.

To understand the basic of github have a look in the following 
link -> https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/
but you don't need to understand it, especially if you're keen on getting on with using your new pucapad.

Step 12: go to the actions tab, click on the hyperlink of the new build, scroll down to artifacts and 
click on firmware to download the zip file to your PC.

Step 13: extract the zip file and you should see a .uf2 file which is the firmware you need 
for the nice! nano of your puca.

Step 14: connect your nice! nano to your PC, put it in bootloader mode -> it should show as a devices on your PC. 
Go in the device folder and copy the new .uf2 file you got from GitHub to the device. 
You should be ready to go! Check whether the keymap and the puca is working as you expected. 

This video should help with Step 12 to 14 -> https://youtu.be/G8cqcFQdHGk

Good luck!
```

