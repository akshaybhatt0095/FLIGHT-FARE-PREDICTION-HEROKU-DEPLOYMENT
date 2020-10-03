<!-- banner  -->
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/Flight%20Price%20predictor.gif" width="1600" height="400">

### PROJECT OVERVIEW
*A machine learning web app that predicts the price of the flight based on several features. The application is built using Flask and deployed on Heroku platform.*
*The model is built using Random forest regressor with a R2 score of 81.38% after going through Hyper Parameter tuning(RandomizedSearchCV).*
### DEMO:
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/Demo.gif" width="1600" height="600">

### LINK
(https://ml-flight-price-prediction.herokuapp.com/)

### MOTIVATION 
* Understand how the machine learning project cycle works where the deployment plays a crucial part.*

### PROJECT AIM
*Prices of flight ticket varies abruptly and it becomes hectic for a user to decide on different deals. A flight fare prediction model will help travellers with the optimal time to plan their travel and understand the trends in the airline industry.*

### TECHNOLOGIES USED
<img target="_blank" width="60px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png"/><img height="60" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/jupyter-notebook/jupyter-notebook.png">
<img height="60" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/scikit-learn/scikit-learn.png">
<img target="_blank" width="60px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png"/>
<img target="_blank" width="60px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/css/css.png"/>
<img target="_blank" width="60px" src="https://raw.githubusercontent.com/github/explore/78df643247d429f6cc873026c0622819ad797942/topics/github/github.png"/>
<img target="_blank" width="55px" src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/images.png"/>
<img target="_blank" width="60px" src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/heroku(1).png"/>

### PYTHON LIBRARIES USED
* Numpy 
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn
* Plotly
* Missingno

### MACHINE LEARNING MODELS TRIED
* Random Forest
* KNN
* Ridge regressor
* Lasso regressor
* Decision Tree regressor
* XGB regressor

### PROJECT WORKFLOW
* PROBLEM DEFINITION
* DATA LOADING 
* [DATA PRE-PROCESSING](### DATA PRE-PROCESSING)
* [FEATURE EXTRACTION](### FEATURE EXTRACTION)
* [EXPLORATORY DATA ANALYSIS](### EXPLORATORY DATA ANALYSIS)
* [DATA ENCODING](### DATA ENCODING)
* [FEATURE SELECTION](### FEATURE SELECTION )
* [MODEL SELECTION](### MODEL SELECTION )
* HYPERPARAMETER TUNING
* CREATE A PICKLE FILE
* BUILD A FLASK APP
* DEPLOYMENT OF MODEL ON HEROKU

### DATASET INFO
* The dataset is taken from Kaggle - (https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh)
* Dataset contains 10683 rows and 11 columns
* Features - Airline , Date of Journey, Source, destination, Route, Departure time, Arrival time, Duration, Total Stops, Additional info

### DATA PRE-PROCESSING
* Dropped two records with missing values
* Dropped 220 rows having duplicate records

### FEATURE EXTRACTION
* Dropped the route column as we already have source and destination columns
* Converted Total stops column(categorical) to numerical values
* Extracted date time features from Date of Journey column:
  * Day
  * Month
  * Year
  * Weekday
  * Week Number
  * First half or Second half of the month 
* Extracted time features from Arrival and Departure time (Hour and Minute)
* Generated total duration of travel in hours and minutes
* Extracted flight arrival and departure category in terms of time
  * Morning ( 5am to 11am)
  * Afternoon ( 11am to 4pm)
  * Evening (4pm to 9pm)
  * Night ( 9pm to 5am)

### EXPLORATORY DATA ANALYSIS

* PRICE v/s AIRLINE
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(389).png" width="1600" height="600">

* AIRLINE COUNT
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(390).png" width="1600" height="600">

* MONTHLY FLIGHT COUNT
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(391).png" width="1600" height="600">

* SOURCE v/s PRICE
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(398).png" width="1600" height="600">

* DESTINATION v/s PRICE
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(399).png" width="1600" height="600">

* MONTH v/s PRICE 
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(400).png" width="1600" height="600">

* DEPARTURE AND ARRIVAL CATEGORY 
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(401).png" width="1600" height="600">
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/EDA/Screenshot%20(402).png" width="1600" height="600">



### DATA ENCODING
*As the machine learning model can only read numerical values we need to encode categorical features into numerical values.*
Nominal data - One hot encoder is used 
Ordinal data - LabelEncoder is used 

### FEATURE SELECTION 
*Feature Selection is the process where you automatically or manually select those features which contribute most to your prediction variable or output in which you are interested in. Feature selection reduces overfitting, improves accuracy and reduces training time. 3 important techniques of feature selection are:*
* Univariate Selection
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/img/Screenshot.png" width="1600" height="600">
* Feature Importance
<img src="https://github.com/akshaybhatt0095/FLIGHT-FARE-PREDICTION-HEROKU-DEPLOYMENT/blob/master/img/Screenshot%20(4.png" width="1600" height="600">
* Correlation Matrix with Heatmap
Correlation matrix doesn't go well with this case as we have have too many features.

### MODEL SELECTION 
I have tried 6 regressor models of which random forest regressor performed really well.

Here are the test scores for the models:
* Random Forest - 83.24%
* KNN - 52.2%
* Ridge regressor - 58.6%
* Lasso regressor - 60.7%
* Decision Tree regressor - 73.9%
* XGB regressor - 83.03%
Random forest regressor model and XGB regressor model performed really well compared to other algorithms.


### FUTURE SCOPE
* WORK ON LARGER DATA
* IMPROVE FRONT END WEB DESIGN
* Scalability
























