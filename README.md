iam
===
iam is a simple script to keep track of what you are doing.
Useful if you often work at command line and are often interupted.

Installation
------------
Put iam in your path (~/bin is usually a good place) and make it executable

Usage
-----

    $ iam -h 
    USAGE: iam [option | message]
    
    Options
    -l  Lists the last ten entries
    -c  Clears the history
    -e  Allows you to directly edit the history file
    -m  Mark the history with current timestamp
    -h  Displays this message

    With no option, iam will either show the last entry or store a new entry if the message is present.

Examples
--------

1) You are working when a colleague wanders over and starts talking. Before you get derailed, make a note.

    $ iam just about to update IndexController.php with user details

Your colleague chats away and then finally leaves

    $ iam
    At 20:23 on 22/01/2013  I was just about to update IndexController.php with user details

Ah yes. That was it.

2) You are called to go to a meeting.

You think this may put you behind. Better make a note of how long it goes on for

    $ iam going into a meeting

Have meeting the meeting and get back

    $ iam -m
    $ iam -l
    At 10:26 on 22/01/2013  I was going into a meeting
    At 12:54 on 22/01/2013  --MARK--

You decide you want to make that read a little better

    $ iam -e

Edit the line to replace "--MARK--" with "I was back at my desk"
To see the new list

    $ iam -l
    At 10:26 on 22/01/2013  I was going into a meeting
    At 12:54 on 22/01/2013  I was back at my desk
