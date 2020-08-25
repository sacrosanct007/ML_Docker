# ML_Docker

**Data Science Docker steps**
1. Go to command prompt (cmd) and change directory to C:\Users\aditi\OneDrive\Desktop\ML_Docker (Replace with your local folder where "docker-compose.yml" is located and where you     want to save work )  
	cd C:\Users\aditi\OneDrive\Desktop\ML_Docker  
2. Now run query 'docker-compose up'  
3. Then the command prompt will provide a link which you can open on chrome and your work will be automatically saved in directory C:\Users\aditi\OneDrive\Desktop\ML_Docker
Also when you want to save the requirements.txt you can use !pip freeze > requirements.txt in your jupyter notebook

Reference: https://towardsdatascience.com/jupyter-data-science-stack-docker-in-under-15-minutes-19d8f822bd45

-------------------------------------

**ML Model deployment using Flask steps**

### Prerequisites
You must have Scikit Learn, Pandas (for Machine Leraning Model) and Flask (for API) installed.

### Project Structure
This project has four major parts :
1. model.py - This contains code fot our Machine Learning model to predict employee salaries absed on trainign data in 'hiring.csv' file.
2. app.py - This contains Flask APIs that receives employee details through GUI or API calls, computes the precited value based on our model and returns it.
3. request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
4. templates - This folder contains the HTML template to allow user to enter employee detail and displays the predicted employee salary.

### Running the project
1. Ensure that you are in the project home directory. Create the machine learning model by running below command -
```
python model.py
```
This would create a serialized version of our model into a file model.pkl

2. Run app.py using below command to start Flask API
```
python app.py
```
By default, flask will run on port 5000.

3. Navigate to URL http://localhost:5000

Enter valid numerical values in all 3 input boxes and hit Predict.

If everything goes well, you should  be able to see the predcited salary vaule on the HTML page!

4. You can also send direct POST requests to FLask API using Python's inbuilt request module
Run the beow command to send the request with some pre-popuated values -
```
python request.py
```
