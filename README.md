# DS-USFLab1
Repo for the first lab and student org activity for DS@USF 

## DS@USF - Lab 1

You have been asked as a researcher to analyze the iris dataset which is a collection of features (columns) which descibe the lengths of different parts of a flower in a series of observations, or "examples." 

### A comment on "features" and "examples"
As you can see, the language we are using for columns and rows (features and examples) are a bit different when approach the dataset as data scientists, because we will treat the _model_ we will be using as a "student" which is trying to predict the underlying relationship in the dataset. The rows in the dataframe represent the "examples" our "student" will use to uncover the underlying relationship between our features in our dataframe. 


### Exploratory Data Analysis 

The first step in this data science workflow is to analyze the data (the data has already been extracted for us). Using tools like R and Python help us do this because they already have packages embedded in them where we can begin asking very specific questions of our data. If you have taken SQL, think of these packages as a very flexible set of querying tools. If you come from the spreadsheet world, think of the packages as easy ways to filter and pivot through an excel sheet. 

To begin, install dplyr on your computer by running this code:
_it's not necessary to this if you have already installed the package_
``` r
install.packages("dplyr")
# notice that you need to put the name of the package in strings: ""
```
We are working in the R environment, which means that we need to let R know that we intend to use the package in our analysis. **You must load the libraries before your script everytime so that it works for the rest of the script**
``` r
library(dplyr)
# Here, you don't need to put the name 
# of the package in strings
```

#### Examples with the "flights" dataframe

You will use dplyr to generate some insights in the form of a table and basic statistics. In this example, we use the "select"  keyword to choose only specifi columns from the "flights" dataframe. 
``` r
select(flights, year, month, day)
```

In this example, we used the 'select' keyword to only grab the year, month, and day column from the _flights_ dataframe.

Here we will use another keyword 'mutate' to create a new column in our dataframe.
``` r
mutate(flights, #use the keyword
gain = arr_delay - dep_delay, # we create a NEW column 
speed = distance / air_time * 60 # We create ANOTHER column
)
```
