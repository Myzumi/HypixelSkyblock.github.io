# Explanation of what occured on the 5th of May 2021

On the 5th of May 2021 there was a change to the server system that hosts a large majority of the bots and databases relating to the Hypixel Skyblock server. 
A new webserver was added, and while this was added, an old webserver was deleted (with a bot that wasn't being used anymore).

The problem occured when we figured out that the punishment, level and reputation data databases all also sat on that server, because of some poor planning at the time.
This was bad news for multiple reasons. Firstly, everyone's punishment history was wiped, allowing them to have a clean sheet (e.g. no previous punishments were kept).
Secondly, people's levels and reps were deleted, which they often worked really hard for.

I (Skezza) set up the punishment system in a way to allow for redundancy, and could regenerate the database data by looping over every embed in a channel, so all that data was successfully recovered.
The problem with the reps and levels was still a problem.

A quick and non-complete fix was to give everyone with the active roles the level required for that active role (e.g. active requires level 15, so if they have the role, set their level to 15 again).
This obviously has a shortcoming that everyone could lose up to 14 level (worst case scenario e.g. 29 would go back down to 15).
Another thing we did was to give the people on the leaderboards their exact level back, meaning for the people who needed it most, their levels (and reps) were recovered.

The server was backed up right before it was deleted, however the software that handles the servers, for some unknown reason, doesn't backup the database that's on the server, so although we recoverd the server, the database was gone.

What we're going to do moving forward:
We've already moved the databases onto their own servers, which will prevent accidental deletion going forward.
We have configured the backups to also backup the databases.
We are trying recover the data using data recovery software.
We will give boosts so that people can recover what was lost.

If you have any questions, I'm happy to answer them, message me at Skezza#1139 and I'll be happy to explain anything else.

We're sorry this happened, nobody likes it when this stuff happens, but we're trying our best to make this as unnoticable as possible so your user experience isn't hindered.

-Skezza
