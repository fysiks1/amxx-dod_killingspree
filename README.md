# DoD Killing Spree - Written by Vet(3TT3V) for Day of Defeat 1.3

## Description
This plugin simulates the 'Bonus Round' found in DOD:S. In that, when a team
wins, the winners are allowed to 'mop up' on the losers. During a killing
spree, the losers have weapons stripped (can optionally keep a knife/spade),
the spawn protection entities are disabled, the killing spree is announced
by HUD and soundbite, and an OSD is displayed to show the time remaining.
Losers are prevented from picking up dropped weapons. Also, control points
and control areas are disabled.

## Commands
dod_killingspree (access level 'h') - Toggles the plugin on|off

## CVars
- dod_killingspree_enable <0|1> - Disable/Enable the killing spree plugin (default 1)
- dod_killingspree_time <##> - Killing spree time (default 15 seconds, 11 minimum)
- dod_killingspree_knives <0|1> - Give knives/spades to losers? (default 1 - yes)
- dod_killingspree_stamina <0|1> - Give winners unlimited stamina? (default 1 - yes)
- dod_killingspree_respawn <0|1> - Allow respawns during killing spree? (default 0 - no)
- dod_killingspree_notify <0|1> - Enable notify message and soundbite? (default 1 - yes)
- dod_killingspree_osd <0|1> - Enable countdown OSD? (default 1 - yes)
- dod_killingspree_message <string> - Notify message to show on HUD

## Config file (killingspree.cfg)
This plugin uses a config file to set several options during a killing spree.
Plugin pausing, allows you to pause specific plugins during a killing spree.
For example, the WeaponMod2 plugin will still give a loser a weapon if they
say /bar during a killing spree. So you'd want to pause this plugin.
Server CVars can be set/reset during the killing spree. In the default config,
Friendly Fire has been turned Off, Alltalk is turned On and the Chase Cam is Disabled.
All CVars are returned to their previous state after the killing spree ends.
Option to disable teleports (used as spawn protection on some maps).
The file MUST have all sections.
Data within those sections is optional. I have included a config file that will
work well for most servers. Information for each section is in the config file.
Please know what you are doing before modifying.

## Compatibility
Compatibility issues with other plugins is not addressed. If compatibility problems arise,
try listing this plugin elsewhere in the plugins.ini file. Or try pausing the other plugin
in the killingspree.cfg file. Other than that, I offer no support.

## Version History
- 3.0 - Added option for unlimited stamina for the winning team
  - Fix problem with player joining the server during killingspree
  - Fix live grenades exploding on following round
- 2.9 - Fix for dod_escape bridge capturing during spree
- 2.8 - Fix occasional runtime error on Linux servers
- 2.7 - Fix for players with deployed weapons
- 2.6 - Fixed func_tank, code improvements
- 2.5 - Original release

## Notes
Has been tested on Windows and Linux using Amxmodx v1.80.
Requires the HamSandwich module.
Uses the killingspree.wav sound file located in the 'sound/misc/' folder