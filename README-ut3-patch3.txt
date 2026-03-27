
This is the third patch for Unreal Tournament 3. Please provide any and all
 feedback on this patch at:

     http://utforums.epicgames.com/forumdisplay.php?f=21.


Gameplay:

- Fixed overlay mesh showing up on hidden sniper rifle when un-zoomed.
- UTGame.bNoCustomCharacters is now globalconfig.
- Now hear own auto-taunts.
- Fix for Liandri bots riding high in vehicles.
- Fixed mutators disappearing between matches.
- Fixed up PC DLC screenshots and player counts.
- Vipers can no longer be driven around underwater if entered while
  underwater - they pop up out of the water, even if deep in it.
- Fixed announcements not playing properly in WAR-MarketDistrict during the
  campaign.
- Fixed manta crouch exploit.
- Fixed loaded RL switching away before releasing load on net clients.
- Fixed occasionally getting stuck when getting up from ragdoll.
- Fixed ending zoom when go into feign death.
- Fixed giving proper stats credit for translocator telefrags.
- Fixed giving proper suicide stat credit for certain environmental suicides.
- Fixed Hoverboard foot placement when watching other client get on.
- Improved the turret controls on the rail turret with analog controller.
- Fixed friendly fire mutator showing up as option for Duel.
- Fixed bug where second enforcer wouldn't show up if picked up while
  switching to enforcer.
- Fixed shock/instagib beams which were grabbed from emitter pool sometimes
  incorrectly having DPG_Foreground set.
- Fixed "missing required file for demo playback" error message.
- Fixed redeemer explosion on client when shot down.
- Fixed big head mutator head scaling popping out at distance.
- End the match right away in duel if a player leaves.
- Fixed not getting kismet node destroyed event when node captured by orb.
- Fixed effect showing up for disabled weapon lockers.
- Don't modify power core damage caused by kismet.
- Fixed scavenger legs disappearing in kill volumes.
- Deployables can no longer be deployed onto hover/flying vehicles.
- Fixed Hoverboard script warnings and possible crash if hoverboard fails
  to spawn.
- Fixed impact hammer impact camera shake for low gore clients.

 

Engine/Rendering:

- Added motion blur menu option for PC (defaults to off).
- Fixed zero extent collision bug in octree code (finding nodes in Z axis).
- LOD Hysteresis / LOD Decision making bug fix.
- Fixed default mesh not having proper LOD settings.
- Fixed rare darkwalker physics crash.

 

User Interface:

- Added player name list to server browser.
- Added midgame map voting, with serverside config options in UTGame.ini:
- bMidGameMapVoting: Enables/Disables midgame map voting
- MapVotePercentage: The percentage of votes required to initiate a map
  switch, counts down based upon VoteDuration;
- NOTE: When VoteDuration=0, votes for a single map must exceed this
  percentage, but when VoteDuration is not 0, the number of players
  voting must exceed this percentage
- MinMapVotes: The minimum number of players that must vote in order to
  initiate a map switch.
- InitialVoteDelay: Delays the enabling of map voting for this many seconds
- Fixed History being saved for servers joined via cmdline and console.
- Fixed leading vote count indicator when map voting underway.
- Don’t show muted talking player portraits on HUD.
- Simple crosshair tweaks.
- Added the number of files left to download to the package downloading
  message.
- Fixed Krall portrait.
- Fixed clipping vehicle HUD beacon when not visible.
- Fixed endgame timer so that it isn't affected by changes in game speed
  (also fixes vote timer)
- Fixed SPMA deploy icon offset.

 

Networking:

- Fixed network vulnerability
- Always sort relevant actors by priority.  Should fix the weird
  actors/properties never getting replicated issues.
- Fixed gibs not showing for clients of listen server if the gibbed player
  wasn't visible to the server player.
- Fixed gibs not showing for clients of low-gore listen server.
- New dynamic netspeed adjustment system for listen servers.  Improves
  network performance for listen servers which typically have limited
  upstream bandwidth by dividing available bandwidth between clients.
  Configurable through new properties in UTGame.ini:
      TotalNetBandwidth=32000 (total upstream bandwidth to be apportioned)
      MaxDynamicBandwidth=7000
      MinDynamicBandwidth=4000
- Fixed "you have lost the match" messages to spectators at end of duel
  match.
- Fixed cases where GameSettings cache in the GameInfo wasn't properly
  getting NULL'd out on DestroyOnlineGame().
- HTTP redirect with compression now falls back to the uncompressed case
  if the compressed file could not be found.
- Fixed erroneous "connection failed" error when performing non-seamless
  travelling.
- Fixed hoverboard link failure sound playing in the world and
  being replicated.
- Fixed low gore clients seeing gibbed players as headless if playing on
  full gore server.
- Increased tracked turret net priority
- Fixed Hoverboard networking replication issues (hoverboard now
  smoother in net games).

 

Server administration:

- UWeb fixes for WebAdmin.
- Fixed downloaded cooked maps not being loaded correctly in some
  cases when requested by the server at initial connect time.
- Fixed net object count problem when using the conformed/cooked audio
  packages in PS3ModTools.  Fixes some networking issues for custom maps.
- Final fix for packagemap problem with going from DLC -> RTM maps.
- Fixed properly showing number of players needed for match to start
  when minplayers is set and bots are enabled on the server.
- Fixed bug with PlayerID being reused for bots after a seamless travel.


Mod support:

- Added support for Interactions to have a PostRender call (to render
  to canvas).
- Added support for Interactions to have exec functions be called on them.
- Added cut/copy/paste support to the console.
- Added Deproject() to canvas.
- Fixed base InventoryManager implementation of GetWeaponRatingFor().
- Fixed crash when placing a new UINumericEditBox in UI editor.
- Fix for custom factions in the UI.
- Added optional flag for ScriptedTextures to skip next clear so that a
  ScriptedTexture client doesn't need to draw every texel of the ST
  every update.
- Added support for -mod commandline option so that a TC mod can have a
  .ini file "sandbox" - where they can have new content paths, new
  startup maps, etc..
- Improved system for getting camera death effect.
- Implemented fix from Aegia for an NxFluid crash.
- Fixed beams not rendering in Cascade.
- Fixed crash when updating a UIPrefab.

 
Map specific:

- Fixed CTF-Searchlight black boxes before match starts.
- Fixed CTF-Searchlight search lights.
- Fixed CTF-Hydrosis collision issues.
- Fixed DM-Morbias collision issues.
- Fixed collision issue in DM-Deck.

 
AI improvements:

- Fixed bots not using link gun beam on enemies.
- Better bot celebration management.
- Fixed bots doing multiple end of match celebration taunts.
- Improved impact hammer AI.
- Improved darkwalker AI support for crouching under obstacles.
- Improved bot hoverboard AI.
- Fixed bots sometimes not picking up flags/orbs they dropped.
- Fixed bots never spawning in if initially not enough playerstarts.

----------------------------------------------------------------------

Changes from the first and second patches are also included.
 Please see README-ut3-patch2.txt

// end of README-ut3-patch3.txt ...

