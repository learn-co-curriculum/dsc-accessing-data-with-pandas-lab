
# Accessing Data within Pandas - Lab

## Introduction

In this lab we're going to get some practice with accessing data from our Pandas Series and DaatFrames.

## Objectives
You will be able to:
* Understand and explain some key Pandas methods
* Use simple selectors for series
* Access DataFrame data by using the label
* Perform boolean indexing on both Series and DataFrames
* Set new Series and DataFrame inputs

# World Cup Matches

### Load the WorldCupMatches.csv file as a pandas dataframe.


```python
# Your code here
```

### Subset the DataFrame to only rows where the Home Team Name is populated.


```python
# Your code here
```

### How many of the matches were in Montevideo?


```python
# Your code here
```

###  How many matches were played where the home team's name contained a (capital) 'M'?


```python
#Your code here
```

### How many matches did USA play in 2014?  

Hint: they could have been home or away.  

You can combine conditions like this:  
df[(condition1) | (condition2)] #Returns rows where either condition is true  
df[(condition1) & (condition2)] #Returns rows where both conditions are true  


```python
# Your code here
```

### How many teams played in 1986?


```python
#Your code here
```

### How many matches were there with 5 or more total goals?


```python
# Your code here
```

## Summary

Congratulations! You've got some experience accessing data within Pandas Series and DataFrames! Next we'll be moving on to learn about how to perform statistical analysis on data within Pandas.
