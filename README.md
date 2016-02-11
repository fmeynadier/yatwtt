# yatwtt
Yet another Taskwarrior time-tracker

A (very limited) attempt to add some time-tracking abilities to
[Taskwarrior](http://www.taskwarrior.org), work in progress.

## Status update :
I more or less gave up on trying to reimplement a time-tracking system around Taskwarrior... But I found Gnome's [Hamster](https://github.com/projecthamster/hamster) time-tracker to be quite usable, so instead I now use a hook to track time there instead. This hook is very small and can be found here : 

https://github.com/fmeynadier/taskwarrior-hamster-hook.


##Goal 
The aim here is to embed the data within the tasks (so it should be OK with
servers), using "start" and "stop" TW commands as inputs, but keeping the
possibility of altering it a posteriori to correct for mistakes or acknowledge
some work done in the past.

The «traditionnal» way to do so (storing data in the annotations) makes those
annotations overcrowded and useless, and it is not very safe to edit.

##Roadmap :

- Write a hook that stores start/stop date in an UDA (e.g., "timetracking")
- Modify the [tasktime](https://github.com/svenhertle/tasktime) script to take
  this data into account
- Write scripts that allow to manipulate those dates easily, i.e. commands like
  'task N started 2h ago' (start date set 2 h in the past, still active), 'task N worked 3h' (start date set 3h in the past and stop date set now), etc...
- Write conversion script that moves start/stop annotations into the new UDA
 

