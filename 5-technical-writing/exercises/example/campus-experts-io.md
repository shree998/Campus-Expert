# http://githubcampus.expert

This repo contains the website and profiles of all the GitHub Campus Experts. By issuing a pull request you can add yourself to the map and profile list or contribute to the site itself.

# Privacy Notice

**Please** consider safety and privacy of yourself and others before adding / ammending your data or anyone elses.

- Do you want to display a full name? You can leave out the full name field and only include a shortname or nickname.
- For the latitude and longitude, please do not set your home, or an exact place on campus you can always be found. I recommend setting the center of your campus. 
- Do you want to display a profile picture? You can use an avatar or your university crest as alternatives.

# How to add a profile

Create a branch and do the following: 

## 1. Edit _data/experts.yml

Complete an entry in the [experts.yml](./_data/experts.yml) file.

## 2. Create _experts/YOUR-USERNAME.md

Create a new file inside [`_experts`](./_experts) with your username. Ensure you use the same text casing here as you used in step 1.

```
---
layout: profile
title: YOUR-USERNAME
author: YOUR-USERNAME
---
```
