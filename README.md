This code is created with the use of ChatGPT, and it may therefore be some buggs. 
I'm no coder so i'm lacking the ability to streamline the code.

I made this for my own use and my specific needs, feel free to use and develop!
My critera was to make a script that was fast, and that also sort and named the files correctly.
It takes about 45-60 seconds to create and sort ~150k of .strm-files. 

Also see advanced settings in "strmcreator_main" for some CPU utilazation and also the ability to change the url (ex route via a proxy instead of the provider). 

======HOW TO USE======
1. Edit the settings in "strmcreator_whitelist"
2. Run "strmcreator_whitelist.py" using
```
python3 strmcreator_whitelist.py
```

It will create a new textfile containing every group from you m3u playlist. 
As default all groups will be disabled.

3. Edit the new "group_whitelist.txt" and remove the # in front of the groups you want to use.

4. Edit the settings in "strmcreator_main.py". See comments for some guide/help.

5. run "strmcreator_main.py" using
```
python3 strmcreator_whitelist.py
```

Your .strm files should have been created and sorted accoring to your settings. 
