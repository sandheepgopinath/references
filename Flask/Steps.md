# Steps to deploy a Flask App

1. 	Install Flask
	- pip install Flask
2. Define structure of project
	- main.py : Python code of Flask web framework
	- requriements.txt : Dependencies
	- app.yaml L Helps google App Engine decide which settinsg to use on its server
3. Create a Virtual Environment
	-  Create environment
	
			python3 -m venv tf_classification
        
	- Activate environment 
			source tf_classification/bin/activate
    - Add the requirements.txt file with all dependencies
    - Create app.py with flask python code and html pages inside template folder if needed
    - Configure Flask
    		$ export FLASK_APP=sample
			$ export FLASK_ENV=development
			$ flask run

# Hosting on Heroku
- Create virtualenv with pipenv and install Flask and Gunicorn

		$ pipenv install flask gunicorn 
- Create a “Procfile” and write the following code. 
		$ touch Procfile
        
 