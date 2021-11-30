# ValorantRankedPointsBot
Discord bot that shows ranked point movement using Valorant's Private/In-Game API and match summary using Tracker Network API.

## Usage
```
-link [Riot ID]
```
Link your Riot ID (name#tagline) to your Discord ID.
```
-login [username] [password] (optional)
```
Use `-login` to link your Valorant player ID with your Discord ID through RSO.
```
-recent <!@user_id> (requires login)
```
View ranked rating of last 3 matches of user (sends webrequest to Valorant API and returns JSON where it is then parsed and displayed). React to display graph of ranked rating history.
```
-match <!@user_id>
```
Shows summary of most recent match of user.
```
-profile <!@user_id>
```
View profile of user (rank, winrate, k/d ratio, ADR, headshots %, time played)
```
-track <!@user_id> | -untrack
```
Track user to auto receive most recent competitive match summary through DM. Use `-untrack` to stop tracking.

## Setup

* Install requirements
```
python -m pip install -r requirements.txt
```
* Store discord token in .env
```
DISCORD_TOKEN=<token>
```
* Enter and store any Valorant username and password (Feel free to create a new one if you don't want to use your main) in .env
```
USER_NAME=<username>
PASSWORD=<password>
```
* Enter mongodb uri in .env
```
DATABASE_URI=<URL>
```
* Run the bot
```
python bot.py
```
