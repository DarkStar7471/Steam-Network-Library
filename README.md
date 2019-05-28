# Steam Network Library
*A brief guide on creation of a Steam/general game network library, shareable between multiple computers*

**Requirements:**

- Network share for steam games hosted via FreeNAS or another share hosting system
- Plenty of relatively fast storage inside the hosted share
- Gigabit switches to connect you to that share
  - *While this will not be likely something you access from outside your home location, I still suggest having gigabit switches to make your intranet communication nice and speedy*

**How to Set Up Steam Network Share Game Saving**
*This instruction set presumes that you already have a network share either dedicated to steam games or a directory within a share dedicated to steam games. Games saved in this location will work 95% of the time when launched with Steam. This kind of works with Origin, I don’t recommend using it for other than steam games. I’ve had mixed results with some of the crazier games like GTA V that I’ve tried with this but I’m pretty sure this will work even with that nowadays.*

1. Launch Steam
2. Make sure your network drive is mapped with the option to automatically remount on boot.
3. Make sure no files are downloading.
   1. Steam will not allow adding steam library folder locations when other games are downloading, rather it will gray out the option to manage library folders.
4. Navigate to *steam settings*, then to *downloads*. This is the same page that you would use to set your download speeds.
5. On the download settings page, click on the link near the top titled something like *“Steam Download Locations”*
6. Select *add new location*
7. Browse to the location of the share you want to store your steam games on, typically this will be a directory titled Steam Library on your share. Mine, for instance, is named “Steam Deep Storage” as I can manage the saved location and practically have a large percentage of my library downloaded here.
   Once your folder is selected, confirm it and start downloading games to this location. You can also set this to be your primary/default steam download location.

**Key notes:**

- Make sure you always reconnect to your network shares on boot. If steam cannot reach the network shares, it presumes that part of your library doesn’t exist and it forgets about it and you will have to repeat this process. This is where having a domain in play can be really nice as it will automount for you and do so much more consistently. That being said, a domain is also complete overkill for this project.



- You can create a dedicated virtual machine or physical machine to update this library. Simply log-in to steam on the virtual machine (I suggest having multi-factor authentication set up for this to make this more secure), map the network storage, and set it as part of the steam library in steam. **It will automatically update for you and can also act as a network PC that you can stream games from (i.e. Steam in-home streaming) as long as it is powerful enough to play these games.**

  - Keep an eye on these downloads, they add up quickly. I suggest disabling the auto-update on games you do not play very frequently. This will allow you to still have them installed but you just have to wait a short bit when starting them up on occasion, still much much faster than redownloading them altogether (typically 1 gig or so of updates depending on the game versus several gigs to reinstalling the game altogether).



- You can access these games from any computer connected to your network. Don’t push your luck with a virtual private network, latency will be ridiculous until the total internet architecture improves. All you need to do is point the system to these shares and repeat this process. This can be done for different steam accounts and is a great option for when you have family sharing enabled.



- This entire project is a great compliment to the steam link. They go on sale for $5 pretty frequently and you can put skins on them to customize them. I suggest looking into this.
  Attaching games to your network like this opens up a lot of projects. **Go wild**. The sky is quite literally the limit here. You can do this with portable versions of programs (ex: Rufus portable installation). Keep in mind, your phone can connect to SMB shares and other share types. I fully mean it when I say that this project can go down the rabbit hole.  
