---
title: Home Directory Customizations
nav_order: 3
---

# Home Directory Customizations

How I set up my home directory.

## Directory Structure

These are the directories that I make sure to create outside of the ones included in distros.

```
~/Apps
~/code
  + personal_projects
  + scratch
~/DataLocker
~/journal
~/myTrello
~/start_day.bash
```

### Apps

Where my applications go. Pretty straightforward.

### code

Split into two directories (at least, maybe more depending on if I'm working from this laptop or not):

+ personal_projects
  + All of my personal projects (except for myTrello since it's in home anyway.)
+ scratch
  + Random stuff that isn't worth version controlling.

### DataLocker

NOTE: Might delete this soon since I'm not working with other people's data really anymore.

This is where I keep data that other scientists have sent my way to either analyze or work with in some fashion.

### journal

This is my version-controlled journal that I keep.

### myTrello

This is the CLI I built for interacting with Trello. I use it to create Trello cards for the day.

### start_day.bash

This is the script I use to start my day. The contents of which are:

```bash
# Make today's journal entry.
echo "Making today's journal entry"
python journal/mkday.py today

# Make today's to do items.
echo "Making today's Trello to do list"
cd myTrello && pipenv run python myTrello.py daily

```

