# devchallenge.it---qa---2 [![Build Status](https://travis-ci.org/yyeshchev96/devchallenge.it---qa---2.svg?branch=master)](https://travis-ci.org/yyeshchev96/devchallenge.it---qa---2)

**API tests for OpenWeatherMap** - https://openweathermap.org/api

# REQUIRED TOOLS

These external libraries are required to run api test:
1. **NodeJS** - https://nodejs.org/en/download/
2. **Newman** - https://github.com/postmanlabs/newman#getting-started
Using node, newman can be installed by typing the following command in the terminal: 
    `npm install -g newman`

HTML Reporter:
    `npm install -g newman-reporter-html`

To work with tests localy, please download this repository and unarchive files
`git clone URL`

# RUNNING TESTS

**To run the tests, please follow the next steps:**


## Windows:
1. Press Windows button
2. Type "PowerShell" and press **Enter**
3. Navigate to project folder using cd command. E.g.:
	`cd '.\Downloads\devchallenge.it---qa---2\'`

## Mac OS:
1. Open Spotlight (`ctrl + space`).
2. Type "terminal" and press Enter.
3. Navigate to project folder using "cd" command. E.g.:
	`cd ~/Downloads/devchallenge.it---qa---2/`

## Linux:
1. Open terminal (`ctrl + alt + T`)
2. Navigate to project folder using cd command. E.g.:
	`cd ~/Downloads/devchallenge.it---qa---2/`

## All: Once you navigated to project folder, type the following command:
4. `newman run devchallenge-r2.tests.json -e devchallenge-r2.env.json --export-environment devchallenge-r2.env.json -r cli,html`

Test execution result will be displayed in the console

Additionally, html report will be generated in the `newman` folder
