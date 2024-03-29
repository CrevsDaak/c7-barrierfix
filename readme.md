Crevs' impressively small Fixpack
=================================

I've created this fixpack to put together some small fixes that I currently use for my own installs.
Generally, you wouldn't need anything that's provided here, and usage of this fixpack is not exactly encouraged, however the Fireshield component might benefit all users.


Blade Barrier et al infinite damage fix
-----------------------------------------------

This little component does one thing: stop Blade Barrier from instagibbing.

Note that this only occurs either when your game's framerate is set to >30. I haven't investigated enough as to know what exactly causes it, but it happens, quite often even.

What this bug entails is that effects applied via op232 reapply themselves infinitely (or multiple times if not paused) while the game is paused IF one pauses the game in the same frame that the spell would be applied in. This makes Blade Barrier and other similar spells deal ridiculous amounts of damage.

More info and bug reports on [this thread](https://www.gibberlings3.net/forums/topic/37716-blade-barrier-bugfix-for-vbg2-with-tobex-ran-through-wine/).


Effects fixer for BG2:ToB
-------------------------------------------

This tool suppresses every encounter of EE or otherwise invalid opcodes in your game's files, since they cause good ol' BG2 to crash.

Will remove them off .spl, .itm and .cre files. Might do something about .eff files later but I don't think those are affected.


Fireshield-like effects damage loop removal
-----------------------------------------------

This component searches the current install for possible damage loops and patches all corresponding spells, thus cutting off any and all possible damage loops caused via effect using opcode 232 with the "on hit" trigger.

I recommend installing this component the very end of your instal queue because to function properly this component requires for all the possible Fireshield effects to have already been installed.
