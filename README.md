# Analyzing AirBnB Boston data

## Project Description
Link to Dataset: [https://www.kaggle.com/datasets/airbnb/boston]

In this project AirBnB Boston data will be analyzed to answer three questions, namely:

### What factors are the most correlated to the price of a listing?
A list of key words have been extracted from various columns like *"name", "summary", "space", "description", "neighborhood_overview", "notes", "transit", "interaction"*. With that information and including provided information like *'accommodates', 'cleaning fee' etc.*, a correlation bar chart has been created to visualize each variables' correlation to 'price'

### What are the most used words to describe a neighbourhood?
To answer this question, an analysis of the text included in the column *'neighborhood_overview'* has been performed. The overviews have been grouped by neighbourhood and have the text has been seperated into individual words which are then counted to see which ones are the most used. With that information a WordCloud has been created to visualize the most used words to describe a neighbourhoods sentiment.

### What are the best and worst deals in current listings based on the data provided?
In order to answer this question, firstly, a **Linear Regression model** had to be trained to predict the listings prices based on the data provided in the dataset. Then the actual price has been compared to the predicted price and the difference has been taken into account. Visualizations with titles - 10 best deals - and - 10 worst deals - have been created, taking into account the positive or negative difference between actual and predicted price.

### A notable decisions 
1. Price outliers were excluded as it was concluded that they were hindering the accuracy of the model
2. When populating NaN values, the mean for each column has been used, apart from columns *'cleaning_fee' and 'security_deposit'* which were transformed to bool columns which indicate with 1 if the respective service was present and 0 if it was not.

### Future work
A way to increase the models accuracy would include to train models to more accurately populate NaN columns instead of using the column mean


### Technologies used
This analysis was done in **Python3** with the help of the packages **Pandas, Seaborn, Numpy, Sklearn, Nltk and Matplotlib** 

## How to use the project
Download a dataset from the AirBnB Website: [http://insideairbnb.com/get-the-data]
Then paste the file path into the following line of the code:

```
#Importing datasets

listingsDf = pd.read_csv("..your_file_path")
```

Then run the cells

## Credits
This project was created as part of Udacitys Data Science Nanodegree

Inspiration for the second question was drawn from the following kaggle dataset: [https://www.kaggle.com/code/xujiang1993/boston-airbnb]

## Blog post
Link to Blog Post on Medium: [https://medium.com/@pv1g15/how-to-book-an-airbnb-faa832fabfc6]
