# tibberData
1. General:

This project is done to collect and format data from tibber api in bash. 
It is by far not perfect and also not testet in every use case or efficient at all but it works for me. 
You are free to use it in personal/private, non commercial setting if it helps you to manage youre personal tibber data. I cannot guarantee that it works on youre Maschine (you can change youre local version to youre circumstances).

2. Used Technologies:

This project provide some usefull scripts to be able to store, collect, format and graphically show youre personal data from the energy provider tibber (See: https://tibber.com)
It was build on MacOS using these main techologies: (which have to be installed - also please check the paths they are just does i have) 
Bash (tools used on the bash like "jq"): Most of the code is written in Bash scripts
R: Used to build graphical representations of the collected and filtered data
GraphiGL: Used as a querry language to get the data from the tibber api
Python: Some tiny things like dealing with decimal numbers in bash scripts 
Postgress (psql): (planed for the future) to store the collected Data in a Database 

3. How to start:
install all necessury languages and packages (R.app,Python,jq (use homebrew), ...)

- 1. write youre tibber api token (see: https://developer.tibber.com/settings/access-token) into the downloaded script: "tibberDailyPrices.sh" in the var: TOKEN
- 2. run the script "/Users/$USER/tibberDailyPrices.sh" in youre mac terminal (once a day in the best case to get youre tibber prices for today and tomorrow)
- 3. run the script "/Users/$USER/cleanTibberData.sh" to clean all of the previously collectet and stored data into CSV-Files (for each day and also for all days) and also make a png of each day and all days data. 

Now you get the formatet and processed data in youre path "/Users/$USER/tibberData"

Additionaly there are planty of flag's that you can use to further specify the requested behavior.
If you want more information on the given flag's run the script: "/Users/$USER/cleanTibberData.sh -h" or "/Users/$USER/cleanTibberData.sh --help"

4. Feedbaack:

If you find any bugs (there are mostlikly many) or have feedback you can contact me but please dont be sad if I dont have the time to answer.
