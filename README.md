# **Biblio**

## **Contents**

- [**Simon Game**](#simon-game)
	- [**Table of Contents**](#table-of-contents)
	- [**CI Brief**](#ci-brief)
	- [**UX**](#ux)
		- [General Design](#general-design)
	- [**Features**](#features)
		- [Existing Features](#existing-features)
		- [Features left to implement](#features-left-to-implement)
		- [What could be done better](#what-could-be-done-better)
	- [**Technologies Used**](#technologies-used)
	- [**Testing**](#testing)
		- [Tools used for testing](#tools-used-for-testing)
	- [**Changelog and Fixes**](#changelog-and-fixes)
		- [0.0](#00)
		- [0.1](#01)
		- [0.2](#02)
		- [0.3](#03)
		- [0.4](#04)
		- [0.5](#05)
		- [0.6](#06)
		- [0.7](#07)
		- [0.8](#08)
		- [0.9](#09)
		- [1.0](#10)
	- [**Deployment**](#deployment)
	- [**Credits**](#credits)

<hr />

Hello there,  
and welcome to my second [Code Institute (CI)](https://courses.codeinstitute.net/) school project.
In this project I should be able to show that I can work with HTML, CSS and JS as well as create responsive design which works on commonly used devices.

I decided to follow the given example from CI for this project and create a simple **Simon Game**.

<hr />

## **CI Brief**

- **CREATE A SINGLE PAGE APPLICATION THAT RELIES HEAVILY ON ONE OR MORE APIS**
  - Create a site that calls on the Google Maps API and/or the Google Places API (or similar) to allow users to search for their next holiday destination. You'll want help your users:
    - Select a destination city
    - Find tourist attractions
    - Find accommodation
    - Find bars and restaurants
    - Provide search results in a manner that is visually appealing for your user (by drawing on the skills you have learned in User-Centric Frontend Development)

- **CREATE A MEMORY GAME (my choice)**
  - Build a simple single-player memory game inspired by Simon.
  - Check out this short video and Wikipedia entry to understand the rules of the game
  - Provide details in your README.md of the logic you have used to build your game as well as an explanation of how you tested your logic

- **CREATE A DATA DASHBOARD**
  - Build a data dashboard that visualizes a dataset of your choice
  - Your data can be stored locally (e.g., in a js file) or sourced from an API
  - Visualise your data using D3.js and dc.js

- **CREATE YOUR OWN PROJECT**
  - If you choose to create your project, the scope should be similar to that of the example brief above. If you want some ideas, please ask your mentor for advice and direction.

[**To top**](#Table-of-Contents)

<hr />

## **UX**

### General Design

Design | Importance
--- | ---
Functionality | 6
User experiences | 6
HTML / CSS | 5

**The project general idea is for entertainment purpose only.**

- create an application which feels good for the user

[**To top**](#Table-of-Contents)

<hr />

## **Features**

### Existing Features

- **Game menu**
  - `new_game()`
    - allow user to create new profile
      - user can choose from 4 different difficulties ("Normal", "Medium", "Hard" and "Never ends")
  - `load_game_menu()`
    - allow user to load existing profile
    - allow user to delete existing profile
  - `statistics_menu()`
    - allow user to view statistics for finished games
  - `settings()`
    - allow user to play the game without sounds which makes the game harder
    - allow user to play with every sequence randomized which makes the game harder
- **Simon Game**
  - depends on user input the game will create a sequence which user must much exactly
  - if the user is able to match the sequence next round will begin
  - as soon as user match the last sequence he is presented with end game overlay with score screen as well as he has the option to view statistics page or start a new game
- **User**
  - can create unlimited amount of profiles  
  *Only limitation is minimum 4 characters for profile name*

**Please see [**Changelog and Fixes**](#changelog-and-fixes) for full details of the changes and current stage of the application.**

### Features left to implement

- limited tries
  - wanted to add limited tries depends on the difficulty
- statistics
  - add more colours to statistics modal depends on the score. Also `sort()` the results by the score
- different themes
  - old style design will be added in future
- when loading the game the sequence is played again and this can be used to cheat the game. 
  - However, I did not want skip this as after a while user will probably forget the sequence and therefore I left it like that.
- limit sequence replays
  - did not add it as user can play the sequence when game is loaded so it can be cheated anyway
- game settings should not be global, and I should hook the setting to each individual profile. This way the user can get scored based on the setting
- game rules has been removed from the due to the time but will bring it back

### What could be done better

- error handling
  - right none minimum to none. Also not enough feedback to user if something goes wrong
- the whole JS was tested manual therefore more automated tests
- score system is very basic
- load game should show (as soon as implemented) what setting the user plays on
- `README.md`
  - unfortunately the README could be written in more details due to the time left for the project

[**To top**](#Table-of-Contents)

<hr />

## **Technologies Used**

- [Bootstrap v4.0.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
  - The project uses **Bootstrap** to speed up the development.
- [Font Awesome v5.3.1](https://fontawesome.com/)
  - The project uses **Font Awesome** for icons.
- [JQuery v3.2.1](https://blog.jquery.com/2017/03/20/jquery-3-2-1-now-available/)
  - The project uses **JQuery** for better user experiences as well as to speed up the development.

[**To top**](#Table-of-Contents)

<hr />

## **Testing**

The project has been tested on commonly used devices and browsers such as:

- Desktop PC

- Tablets

- Mobiles

### Tools used for testing

- **Front End**
  - [W3C Markup Validation Service](https://validator.w3.org/) (All pages)
    - Document checking completed. No errors or warnings to show.

  - [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/) (All pages)
    - **Sorry! We found the following errors (52)**
    - **Warnings (981)**  
    *Both due to the Bootstrap 4*  
    *There are no errors in custom CSS*  
  - [JSHint](https://jshint.com/) (Report of all custom JS functions)
    - **There are 81 functions in this file**
      - Function with the largest signature take 2 arguments, while the median is 0.
      - Largest function has 28 statements in it, while the median is 3.
      - The most complex function has a cyclomatic complexity value of 7 while the median is 1.
    - **Seven unused variables**  
    *As the functions are called from templates* 
      - random_sequence
      - test_data
      - game_overlay
      - no_feature
      - delete_profile
      - create_game
      - game_menu

[**To top**](#Table-of-Contents)

<hr />

## **Changelog and Fixes**

*[Git](https://git-scm.com/) has been used for version control.*

- There are 13 different branches:

  - [master branch](https://github.com/MiroslavSvec/simon-game/tree/master) Used in production.
  - *12 other branches has been created for development purpose only. Where each branch represent different version of the application.*

### 0.0

- **Changelog**
  - Created html main page for the book search engine
  - Added symbol/logo for the tab

### 0.1

- **Changelog**
  - separated JS to multiple files for better readability
    - [simon.js](/static/js/custom/simon.js) *Game functionality*
    - [main.js](/static/js/custom/main.js) *General functions / Document ready / Events Listeners*
    - [saves.js](/static/js/custom/saves.js) *Functions to work with localStorage*
  - [index.html](/index.html)
    - added `#game-overlay` section for user menu
- **Fixes**
  - `simon_layout()` is not executed every time the user change the size of the screen to prevent unexpected layout *For example when user change to landscape on mobile devices*

### 0.2

- **Changelog**
  - [index.html](/index.html)
    - restyled the game base on user feedbacks
    - changed the ID's of `#game-col-` to match JS build in `.random()`
  - [screens.css](/static/css/custom/screens.css)
- **Fixes**
  - fixed issue with containers ID's as JS was not resizing them properly as there was not element with `#game-col-0` or `#game-col-4` no longer
  
### 0.3

- **Changelog**
  - [saves.js](/static/js/custom/saves.js)
    - added basic structure for creating new game data or `.push()` new game data to existing `simon_save` in `localStorage`
  - [templates.js](/static/js/custom/templates.js)
    - added for holding HTML templates
  - [main.js](/static/js/custom/main.js)
    - added `js_alerts()` animation
  - [index.html](/index.html)
    - added skeleton for game menu to `#game-menu`
    - added new game form to `#game-overlay` (`new_game_template()`)

### 0.4

- **Changelog**
  - [simon.js](/static/js/custom/simon.js)
    - added basic structure for playing sequence

### 0.5

- **Changelog**
  - [templates.js](/static/js/custom/teplates.js)
    - added `no_profiles()` template
  - [testing.js](/static/js/custom/testing.js)
    - to hold testing function and keep them separately from main code
  - [simon.js](/static/js/custom/simon.js)
    - `check_answer()` added functionality to check for user inputs
    - `check_game_end()` added fundamentals for ending the game
- **Fixes**
  - [simon.js](/static/js/custom/simon.js)
    - fixed issue in `game_round()` when sounds and animations will play all ate once (added +1000 `delay`  for every element in sequence)
    - added transparent overlay while playing sequence to prevent user to click on elements before the sequence finish

### 0.6

- **Changelog**
  - [styles.js](/static/css/custom/styles.css)
    - added CSS variables to keep the code clean
    - `max-height` and `max-width` set `600px` as I decided to make the game smaller
  - [index.html](/index.html)
    - redesigned `#game-centre`
  - [main.js](/static/js/custom/main.js)
    - added `add_click_events()` and `remove_click_events()` for more security
- **Fixes**
  - [simon.js](/static/js/custom/simon.js)
    - fixed issue in `check_answer()` with rapid clicks
    - fixed issue with `check_game_end()` as the game was not ending properly

### 0.7

- **Changelog**
  - [index.html](/index.html)
    - added functionality for user to be able to load a game in progress and continue where he finished
    - added fundamentals for Statistics menu
- **Fixes**
  - [templates.js](/static/js/custom/teplates.js)
    - fixed issue with incorrect injecting profile id in `profiles_template()` template
    - added `game_end_template()`

### 0.8

- **Changelog**
  - finished statistics page

### 0.9

- **Changelog**
  - added functionality for user to be able to play with muted sounds
  - added functionality for user to be able to play with all sequences randomized
  - [index.html](/index.html)
    - finished settings modal
  - removed links from `nav` as they are not need it for this project

### 1.0

- **Changelog**
  - added functionality for user to be able to delete a profile
  - validate HTML, CSS and JS

[**To top**](#Table-of-Contents)

<hr />

## **Deployment**

The project has been deployed to GitHub Pages  - [Simon Game](https://miroslavsvec.github.io/simon-game/)

[**To top**](#Table-of-Contents)

<hr />

[**To top**](#Table-of-Contents)

<hr />
  
## **Credits**

**Special thanks to:**

- **Sipo**
  - for creating the sounds for me :)

- everyone for finding few minutes to test the project!  

  All of you gave me constructive feedback which made the project better 😊

[**To top**](#Table-of-Contents)
