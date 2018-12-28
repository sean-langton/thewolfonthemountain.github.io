---
layout: post
title:      "Data Gem Portfolio Project"
date:       2018-12-28 06:39:59 +0000
permalink:  data_gem_portfolio_project
---


**Project Overview**

The goal of the project was to retrieve data from Basketball-Reference.com and be able to display both team summaries and season summaries.

**Scraper Object**

The first class I worked on was the Scraper class and retrieve the raw data from the website. The Scraper class consist of two class methods. The first scrapes all-time data for all active teams from the [NBA & ABA Team Index] (https://www.basketball-reference.com/teams/) by iterating over all rows of the first table on the page that contain the top-level results for each team. The second method scrapes individual seasons for each team by iterating over all by rows of the table provided from a link retrieved from the first method. There is also a custom error built in for if there's an error retrieving data from the website.

**Team & Season Object**

The Team & Season Object consist of methods to initiation new objects when provided with an array of hashes, assign ownership of individual seasons, output a summary of overall performance, and class objects to return all or individual teams/seasons

**CLI**

When the CLI is run, it first runs a method that calls to Scraper class to create an array of teams using data from the website and then calls the Team class to create instances of Team objects using this data. It then runs a method for adding seasons by similarly calling the Scraper and Season class. Once all of the data has been retrieved, it presents the user with a menu. The Main Menu consist of 5 options
1. List All Teams
2. Historical Summary
3. Search By Team Name
4. Search By Season
5. Typing EXIT to Exit

The use selection an option by typing in an option of 1-4, which then results in activating the appropriate method. Option 1 simply iterations over all Team instances and outputs the team name, while Option 2 iterates over all team instances and outputs a brief team summary using an instance method from the Team Class. Option 3 allows the user to search by team name and return both a team summary and year-by-year breakdown, while Option 4 allows the user to search by year and return a team-by-team breakdown.

**What I Learned**

I think I definitely underestimated the difficulty of working on my first project and thought I could complete the project quickly by reusing a significant amount of code from previous labs. However, I think this view actually resulted in the project taking longer than it otherwise would have because I spent a considerable amount of time when starting off trying to force this data and class structure to fit the mold of previous projects. On my next project I will definitely spend more time planning out the structure of the application before diving in. 

I think working on this project has gone a long way in my grasp of coding and understanding concepts. Understanding the difference between class methods and instance methods is something that I only vaguely understood while working on the labs and mostly completely through trial and error, but now I feel I have a firm understanding. Similarly, Git, GitHub, and Gems was something I didn't understand at all and rarely had to interact with during labs as all requirements and repositories were setup for me by the Learn.co IDE. I still have a long way to go with Git as I'm sure it will become more complicated once I'm working within a team but now, I feel I have a basic understanding of the importance of often committing, what it means to push, etc.

