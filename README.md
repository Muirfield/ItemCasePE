<!-- template: startup.md -->


<!-- end-include -->
<img id="ItemCase-icon.png" src="https://raw.githubusercontent.com/Muirfield/ItemCasePE/master/media/ItemCase-icon.png" style="width:64px;height:64px" width="64" height="64"/>
<!-- template: header.md -->

# ItemCasePE

- Summary: An implementation of Bukkit's ItemCase
- PocketMine-MP API version: 2.0.0
- DependencyPlugins: libcommon
- OptionalPlugins: 
- Categories: N/A
- WebSite: http://github.com/Muirfield/ItemCasePE


<!-- end-include -->

<!-- php: $v_forum_thread = "https://forums.pocketmine.net/threads/itemcasepe.8059/"; -->
<!-- php: $copyright="2015, 2016"; -->
<!-- template: prologue.md -->
**DO NOT POST QUESTIONS/BUG-REPORTS/REQUESTS IN THE REVIEWS**

It is difficult to carry a conversation in the reviews.  If you
have a question/bug-report/request please use the
[Thread](https://forums.pocketmine.net/threads/itemcasepe.8059/) for
that.  You are more likely to get a response and help that way.

_NOTE:_ This documentation was last updated for version **1.1.0**.

Please go to
[github](http://github.com/Muirfield/ItemCasePE)
for the most up-to-date documentation.

You can also download this plugin from this [page](http://github.com/Muirfield/ItemCasePE/releases).
Usually there are two types of releases, a _normal_ release (no suffix) and a _lite_
release with the suffix `-lite`.  The _lite_ release has a dependancy on 
the [libcommon](https://github.com/Muirfield/libcommon/releases) plugin, where as
the _normal_ release does not.  You only need to download **one**.


When clonning this repository make sure you use the `--recursive` option:

    git clone --recursive http://github.com/Muirfield/ItemCasePE.git
    
Otherwise you need to initialize sub-modules manually:

    git clone http://github.com/Muirfield/ItemCasePE.git
    cd ItemCasePE
    git submodule update --init --recursive





<!-- end-include -->

A simplistic implementation of Bukkit's ItemCase.

Command:

* /itemcase add

Then while holding an item, tap on a slab or glass block.  This will create an
itemcase with that item.

To destroy, just destroy the block where the itemcase was placed.

## Documentation

Case data is placed on a file in the world folder.  This is
loaded during world load and unloaded during unload.

Available sub-commands:

* /itemcase add  
  Adds an ItemCase with object on hand.
* /itemcase cancel  
  Aborts an `add` operation.
* /itemcase respawn  
  Debug sub-command.  Re-creates all ItemCases.

### Configuring

By default you need to place items on Slabs or on Glass blocks.  This
is **classic** mode.  You can, if you want, enable **new wave** mode.
This would let you place items on any type of blocks.  To enable this,
modify the `config.yml` file:

    settings:
      classic: true

Change the line `classic` from `true` to `false`.

### Permission Nodes:

* itemcase.cmd: allow players access to the itemcase command
* itemcase.destroy: allow players destroy cases

## Changes

* 1.1.0 : Updated
  - Added translations
  - Using libcommon now (2.0.0dev2)
* 1.0.8 : No AIR cases
  - Do not allow to place cases with AIR only.  Reported by @Pub4Game.
    Closes #30.
  - Checks which function to call (isPlaceable/canBePlaced) without having
    to check version.
  - changed isPlaceable for canBePlaced
* 1.0.5 : one-oh-five
  - Added new wave mode that allows you to place itemcases everywhere.
  - Removed callbacktask deprecation warning
  - Fixed bugs and improved permissions.
  - Fixed despawn when chunk unloads
* 1.0.0 : First release

<!-- template: license/gpl2.md -->
# Copyright

    ItemCasePE
    Copyright (C) 2015, 2016 Alejandro Liu
    All Rights Reserved.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.


<!-- end-include -->

