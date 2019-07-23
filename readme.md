Vocabulary Trainer
==================

Motivation
----------
*   Have fun
*   Test the crate vdb

State of the project
--------------------
*   Search for Spanish words in database with ~70000 entries (~30k Spanish words with ~40k English translations, see source below)
*   Automatically match ~700 irregular verbs (see source below)
*   Add results to personal database for review

Used sources for Spanish-English words
--------------------------------------
*   https://github.com/mananoreboton/en-es-en-Dic.git
*   https://github.com/voldmar/conjugation.git

Notes
-----
* My personal database is stored in the project as an example. To remove it and
  start with a fresh personal database, remove the file save/personal.
* While I implement performance optimizations in the database crate, the first
  startup is slow when running in debug mode, ok-ish in release mode.
  Subsequent starts are quite usable even in debug mode for me.
