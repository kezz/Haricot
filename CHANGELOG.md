# Haricot Changelog
This file contains a list of the current changes between Haricot and it's 
upstream fork, Paper. The source for patches that are not created for Haricot, 
and are sourced from other forks, have been linked. Where applicable, 
upstream pull requests are also linked.

# API
* [0002-Fix-NotePlayEvent.patch](patches/api/0002-Fix-NotePlayEvent.patch) - 
  Upstream PR: [PaperMC/Paper/pull/5180](https://github.com/PaperMC/Paper/pull/5180)
  * Deprecated methods on `NotePlayEvent` have been removed.
  * Adds the `getName` method to the `Instrument` enum.
* [0003-More-note-block-events.patch](patches/api/0003-More-note-block-events.patch)
  * Adds two new note block events; `NoteBlockPlaceEvent`and 
    `NoteBlockChangeEvent`.

# Server
* [0004-Fix-NotePlayEvent.patch](patches/server/0004-Fix-NotePlayEvent.patch) -
  Upstream PR: [PaperMC/Paper/pull/5180](https://github.com/PaperMC/Paper/pull/5180)
  * Implements the fixes to the `NotePlayEvent`.
* [0005-More-note-block-events.patch](patches/server/0005-More-note-block-events.patch)
    * Implements the new note block events.