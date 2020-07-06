# Guide to tiling with the KWin window manager

![how it looks](https://i.imgur.com/hPgVWLp.png)
### Intro
I will try my best to make this understandable for anyone. keep in mind my first language isnt english so there might be some wierd stuff lol. and also my neckbeard isnt at its most fluffy today. but i hope this helps or maybe guide you to something you will enjoy. im guessing the reason you are here is because you love tiling. but also maybe love some of the features of KDE plasma. if soo cool, me too! also you should maybe read the guide and steps before starting to see if maybe there is something you need to do before starting. 


### You will need this
1. **KDE Plasma** (ofc), so if you are on ubuntu, pop, or something using gnome. you will need to change your desktop env. GL, not showing that here.
2. **Internet** (but you have it i guess as you are reading this)

# Installing

sike! before actually installing.

### Removing the titlebar
go to **settings** _->_ **Application Style** _->_ **window decorations**. pick breeze, as you need a theme with the options. now dont worry about your global theme. as we are just removing the titlebar.
_(dont worry there is a shortcut for all of the titlebar buttons, but you dont need those for tiling anyway. thats kind of the point of a tiling window manager.)_

select Breeze, click its edit button(looks like a pen). a window should pop up like the one under.
![popup](https://i.imgur.com/ClKoWeW.png)

now as in the picture, click the 'Window-specific Overrides'. click Add. and now in the text field called Regular expression to match, add `.*` then check the hide window title bar, and click ok and ok.

Tadaa, now you still have borders and shaddows, but no tilebar. 

### Borders
Shaddows are adjusted in its own tab of the pupup we just worked on. the borders are at the bottom of the settings page we are in like shown under, and not in the pupup.
I would use the 'normal' thickness for borders and shaddows are up to you.

![border](https://i.imgur.com/3NbvyiC.png)


To get the colored borders. you need to edit the ```kdeglobals``` file.

that file is located in your .config folder.
You should make a copy of it. and rename it something like ```kdeglobals.old``` so you have a copy of the original.

at the bottom of the file under the ``[WM]`` section. This is where you might have to add the lines you need. i highlighted the lines in the picture below.
![how it looks](https://i.imgur.com/gU9YODx.png)

the colors you need have to be in RGB format.
```
frame=153, 211, 255
inactiveFrame=38, 38, 38
```

When you save after the edit. The borders might all go white. Dont worry just log out and back in again. This should be all you need to get the borders done. 
Now the border color will be different on the window who has focus. i suggest going into syste settings, and set a keybinding to change focus.


### top bar
now also be a good time to add something to your top bar.
 
![bar](https://i.imgur.com/mf96aDK.png)

right click your bar, and click 'add widgeets' (the nice big plus symbol). The ones im using here is called 'Global Menu' for the menu, and 'Window Title' for the icon and window class. if its not already in your widgets just click the 'get new widgets and look for it there'


## Installing the tiling script.

Well. here you need to go to the creator of the script and follow his guide. Its very easy to install. just follow that and then come back here after intalling.

[The Script](https://github.com/kwin-scripts/kwin-tiling)


now that its installed, open systemsettings again.
under Workspace, go to KWin scripts. and you should se a script called 'Tiling Extension'. like in the picture below.
![settings](https://i.imgur.com/kRunt3h.png)

then click the settings wheel another pupup should show up.__if there isnt a wheel there, run this in your terminal:__
```
mkdir -p ~/.local/share/kservices5
ln -s ~/.local/share/kwin/scripts/kwin-script-tiling/metadata.desktop ~/.local/share/kservices5/kwin-script-tiling.desktop
```
this will be the settings for the gaps and such. the first tab, make sure to not check the 'remove borders' as we have worked so hard on our borders lol.

### Gaps
next tab, the gaps. here i use 15 on left, right, bottom and top.
and under that i use 10. this might change with your monitor size im guessing. do what works for you.
then click ok

![gaps](https://i.imgur.com/1i67GqB.png)

now you should be done. there is a cheat sheet at the script creators page. but i have also made a 'fake' man page for my self that im guessing some others also might like.
***
## Manual(ish)
so what i did is i added and the sheet of commands into a txt file. placed it in my home dir. and in my .bashrc added this:

`alias tiling='clear; cat tiling-gelp.txt'`

this way, when i want to know something i can just type 'tiling' in my terminal and i get the help i need.

[Link to the txt file](https://github.com/waltereikrem/tiling-sheet/blob/master/tiling-help.txt) there might be some bindings in that sheet that isnt bound by default tho.

![sheet](https://i.imgur.com/1PJXB5y.png)

also a  couple of shortcuts you might need. if you do super + f to make a window float. you can maximize with super+PgUp, and minimize with super+PgDn. and you can hold alt and left click anywhere on the window to move it around. and hold alt and right click to resize the window. my mostly i guess you would use the tiling rather than the floating
### Hope it helps

Hope this helps you. Im not trash at english, but no professor. so it might be hiccups here and there. I really love how KDE and Kwin have evolved tho. this is my perfect setup. and makes me love linux so darn much. so i hope this works for you guys too. cheers!
