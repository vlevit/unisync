unisync — Unison bash wrapper
=============================

unisync is `Unison <http://www.cis.upenn.edu/~bcpierce/unison/>`_ bash
wrapper. Single unisync configuration file replaces Unison profiles. unisync
automatically constructs roots according to your location. It allows to sync
individual files, group of files and all files at the same time.

Usage
-----

Sync all files::
  $ unisync
Sync individual profiles::
  $ unisync firefox emacs bash
Sync groups of profiles::
  $ unisync configs documents

List all available profiles::
  $ unisync -l
List all available groups::
  $ unisync -g
Print commands but don't run them::
  $ unisync -d
Specify Unison arguments::
  $ unisync [profiles|groups] -auto=false -ignore "Name junk"

Configuration file
------------------

unisync looks up .unisyncrc in the user's home directory. If UNISYNCRC
environment variable is set, it overrides the default path. A configuration file
is a bash file by itself. Look at unisyncrc.example for an example.
