Official Deployment Available At: https://fantasy-basketball-assistant-1078149421009.us-west2.run.app/index

A Fantasy Basketball Assistant Website With Features Including But Not Limited To: 

1. A ranking system to give users an idea of which players are the best performers 
2. A replacement recommender to help users find the highest quality replacements for their injured players
3. A boom/bust system to show users which players are performing better or worse than expected
4. A schedule tracker for NBA teams
5. A trade calculator to determine whether you or your opponent gets more value out of a trade between players

Tech Stack: 

1. Flask backend
2. HTML/CSS frontend
3. Firestore database 
4. GCP cloud scheduler data pipeline from ESPN to firestore
5. GCP cloud build deployment

To Host Application Locally: 

1. python -m venv venv (in vscode terminal)
2. venv/Scripts/Activate.ps1 (in powershell) | (source venv/bin/activate for mac)
3. pip install -r requirements.txt
4. (create a file named .flaskenv in the root directory with FLASK_APP=fantasy.py inside)
5. (after being added to the firestore database, go to project settings -> service accounts -> click generate new private key, and copy absolute path of the json file. Do not put it in the same directory as this repo)
6. (create a .env file in the root directory of this repo with FIREBASE_CREDENTIALS="path to your json file" inside)
7. (this step is optional, but if you want to experiment with espn API, ask for SWID, LEAGUE_ID, and ESPN_S2 and put these variables in the .env file as well)
8. flask run (in powershell with venv activated)
