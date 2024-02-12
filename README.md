Crevs' BG2:ToB impressivelly small Fixpack
=================================

I've created this fixpack to put together the two small fixes that I currently use (though the second one might only be situationally necessary) for my own BGT installs.
Generally, you wouldn't need anything that's provided here, and usage of this fixpack is NOT encouraged.


Blade Barrier et al infinite damage fix
-----------------------------------------------

This little component does one thing: stop Blade Barrier from instagibbing.

Note that this occurs either when Casting Fixes on the ToBEx ini is set to 0, which is necessary to run ToBEx on wine, or when your game's framerate is >30. I haven't investigated enough as to know what exactly causes it, but it happens.

What this bug entails is that effects applied via op232 reapply themselves infinitely while the game is paused IF one pauses the game in the same frame that the spell would be applied in. This makes Blade Barrier and other similar spells deal ridiculous amounts of damage.

More info and bug reports on [this thread](https://www.gibberlings3.net/forums/topic/37716-blade-barrier-bugfix-for-vbg2-with-tobex-ran-through-wine/).


Effects fixer for BG2:ToB
-------------------------------------------

This tool suppresses every encounter of EE or otherwise invalid opcodes in your game's files, since they cause good ol' BG2 to crash.

Will remove them off .spl, .itm and .cre files. Might do something about .eff files later but I don't think those are affected.
