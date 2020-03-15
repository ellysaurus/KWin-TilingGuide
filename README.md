# Guide to tiling with the KWin window manager
![how it looks](https://i.redd.it/nv0wv5x5vzd41.png)
### Intro
I will try my best to make this understandable for anyone. keep in mind my first language isnt english so there might be some wierd stuff lol. and also my neckbeard isnt at its most fluffy today. but i hope this helps or maybe guide you to something you will enjoy. im guessing the reason you are here is because you love tiling. but also maybe love some of the features of KDE plasma. if soo cool, me too! also you should maybe read the guide and steps before starting to see if maybe there is something you need to do before starting. 


### You will need this
1. **KDE Plasma** (ofc), so if you are on ubuntu, pop, or something using gnome. you will need to change your desktop env. GL, not showing that here.
2. **Internet** (but you have it i guess as you are reading this)

# Installing

sike! before actually installing.

### Removing the titlebar
go to **settings** -> **Application Style** -> **window decorations**. pick breeze. now dont worry about your global theme. as we are just removing the titlebar (dont worry there will be a shortcut for all of the titlebar buttons, but you dont need those for tiling anyway rly).

select Breeze, click its edit button(looks like a pen). a window should pop up like the one under.
![popup](https://i.imgur.com/ClKoWeW.png)

now as in the picture, click the 'Window-specific Overrides'. click Add. and now in the text field called Regular expression to match, add `.*` then check the hide window title bar, and click ok and ok.

Tadaa, now you still have borders and shaddows, but no tilebar. 

### Borders
Shaddows are adjusted in its own tab of the pupup we just worked on. the borders are at the bottom of the settings page we are in like shown under, and not in the pupup.
I would use the 'normal' thickness for borders and shaddows are up to you.

![border](https://i.imgur.com/3NbvyiC.png)



now, to get colored borders we need to make a custom color theme. i use 2 actually, because its so easy to use them. the reason we need a custom theme is that, the color of the border is actually called 'Window Background' so this theme for borders are only for windows that use their own background. like your terminal, spotify, Web browser, discord etc.

So! under appearance in system settings. go to **Colors**. pick anyone there and same as before click the edit button. (dont worry we will save as a new theme)
a popup should show up again

![colors](https://i.imgur.com/46yUVLj.png)

here change the window background to the color you want on your border. then save as another theme. maybe like 'tiling border'
then on a window you want the colored border on(and remember not all will work with this as their actual background will change).

* have the window open
* hit **alt** + **f3**
* click **More Actions**
* click '**Configure Special Applicationn Settings**'
* go to the far right tab called 'Appearance & Fixes'
* check the 'Titlebar color scheme', choose 'Force', and pick the theme you just made and click ok

![](https://i.imgur.com/83ruw4I.png)

Now you should have colored borders.


### top bar
now also be a good time to add something to your top bar.
 
![bar](https://i.imgur.com/mf96aDK.png)

right click your bar, and click 'add widgeets' (the nice big plus symbol). The ones im using here is called 'Global Menu' for the menu, and 'Window Title' for the icon and window class. if its not already in your widgets just click the 'get new widgets and look for it there'


## Installing the tiling script.

well. here you need to go to the creator of the script and follow his guide. its very easy to install. just follow that and then come back here after intalling.

[The Script](https://github.com/kwin-scripts/kwin-tiling)


now that its installed, open system setting again.
under Workspace, go to KWin scripts. and you should se a script called 'Tiling Extension'. like in the picture below.
![settings](https://i.imgur.com/kRunt3h.png)

then click the settings wheel another pupup should show up. this will be the settings for the gaps and such. the first tab, make sure to not check the 'remove borders' as we have worked so hard on our borders. and if you want to configure how it works with multiple desktops its here in the first tab aswell

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

[Link to the txt file](https://github.com/waltereikrem/tiling-sheet/blob/master/tiling-help.txt)

![sheet](https://i.imgur.com/1PJXB5y.png)

also a  couple of shortcuts you might need. if you do super + f to make a window float. you can maximize with super+PgUp, and minimize with super+PgDn. and you can hold alt and left click anywhere on the window to move it around. and hold alt and right click to resize the window. my mostly i guess you would use the tiling rather than the floating
### Hope it helps

Hope this helps you. Im not trash at english, but no professor. so it might be hiccups here and there. I really love how KDE and Kwin have evolved tho. this is my perfect setup. and makes me love linux so darn much. so i hope this works for you guys too. cheers!
