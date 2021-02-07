# IBM AI Enterprise Workflow

## Evaluation Criteria
#### Are there unit tests for the API?
unittests/ApiTests.py

#### Are there unit tests for the model?
unittests/ModelTests.py

#### Are there unit tests for the logging?
unittests/LoggerTests.py

#### Can all of the unit tests be run with a single script and do all of the unit tests pass?
run-tests.py

#### Is there a mechanism to monitor performance?
logger.py

#### Was there an attempt to isolate the read/write unit tests From production models and logs?
The segregation is used by prefixing sl_ for production models

#### Does the API work as expected? For example, can you get predictions for a specific country as well as for all countries combined?
app.py 
 
#### Does the data ingestion exists as a function or script to facilitate automation?
cslib.py

#### Where multiple models compared?
model_comparision.py

#### Did the EDA investigation use visualizations?
Used visualizations for during investigation
notebooks/EBS.ipynb

#### Is everything containerized within a working Docker image?
Dockerfile

#### Did they use a visualization to compare their model to the baseline model?
model_comparision.py


# Notes
All commands are from main directory.


To test app.py
---------------------
~$ python app.py

~$ python app.py -d  #  debug mode

basic webpage can be accessed with localhost: http://0.0.0.0:8080/

To test the model
----------------------------
~$ python model.py


Run the unittests
-------------------

~$ python unittests/ApiTests.py

To run only the model tests

~$ python unittests/ModelTests.py

To run only the model tests
~$ python unittests/LoggerTests.py

To run all of the tests
~$ python run-tests.py


Build and Test container
----------------------------------------------
~$ docker build -t capstone .

~$ docker run -p 4000:8080 capstone

webpage: http://0.0.0.0:4000/
