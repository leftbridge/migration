migration
=========

A vulnerable VM made host crash after migration.

Steps to get the diff to kernel v3.7-rc6:
1. Clone kernel source into your local directory: 
$ git clone https://github.com/torvalds/linux

2. Check into the tag v3.7-rc6 
$ cd linux/
$ git tag
$ git checkout -b bv3.7-rc6 v3.7-rc6
$ git branch
* bv3.7-rc6
  master

3. Diff the two directories:
$ diff -Nurp linux/ sched-deadline-mainline-dl/ > aleksi-sched-linux.diff
