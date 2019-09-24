
# Accessing Data within Pandas - Lab

## Introduction

In this lab, we'll look at a dataset which contains information World cup matches. Let's use the Pandas commands learned in the previous lesson to learn more about our data!

## Objectives
You will be able to:
* Use some key Pandas methods
* Access DataFrame data by using `iloc` and `loc` 
* Filter rows of a DataFrame based on given conditions
* Create new columns in a DataFrame

## Load the data

Load the file `'WorldCupMatches.csv'` as a DataFrame in Pandas.


```python
# Import pandas using the standard alias

# Import 'WorldCupMatches.csv' as a DataFrame
df = None
```

## Common methods and attributes

Use the correct method to look at the first 7 rows of the dataset.


```python
# Print the first 7 rows of df

```

Look at the last 3 rows of the data set.


```python
# Print the last 3 rows of df

```

Get a concise summary of the data using `.info()`. 


```python
# Print a concise summary of df

```

Obtain a tuple representing the number of rows and number of columns


```python
# Print the number of rows and columns in df

```

Use the appropriate attribute to get the column names


```python
# Print the column names of df

```

## Selecting DataFrame information

When looking at the DataFrame's `.head()`, you might have noticed that the games are structured chronologically in the DataFrame.

Use the right selection method to print all the information from the 3rd to the 5th game.


```python
# Print rows 3 through 5

```

Now, print all the info from game 5-9, but we're only interested to print out the "Home Team Name" and the "Away Team Name", 


```python
# Print rows 5 through 9 and columns "Home Team Name" and "Away Team Name"

```

Next, we'd like the information on all the games played in Group 3 for the 1950 World Cup.


```python
# Print all info for games played in 1950 for Group 3

```

Let's repeat the command above, but now we only want to print out the attendance column for the Group 3 games. 

You can combine conditions like this:

`df[(condition1) | (condition2)]`  -> Returns rows where either condition is true

`df[(condition1) & (condition2)]`  -> Returns rows where both conditions are true


```python
# Print the "Attendance" column for games played in 1950 for Group 3

```

Throughout the entire history of the world cup, how many home games were played by the Netherlands?


```python
# Number of home games played by the Netherlands

```

How many games were played by the Netherlands in total?


```python
# Number of games played by the Netherlands in total

```

Next, let's try and figure out how many games the USA played in the 2014 world cup. 


```python
# Number of games the USA played in the 2014 world cup

```

Now, let's try to find out how many countries participated in the 1986 world cup.

Hint 1: as a first step, create a new dataset that only contain games in that year.

Hint 2: You can use `.unique()` to make sure you don't end up with duplicate country names.


```python
# Number of countries participated in the 1986 world cup

```

In the world cup history, how matches had more than 5 goals in total?


```python
# Number of matches that had more than 5 goals in total

```

## Changing values and creating new columns

With the information you currently have in your `df`, create a new column "Half-time Goals".


```python
# Create a new column "Half-time Goals" in df

```

Run the code below. You'll notice that for Korea, there are records for both North-Korea (Korea DPR) and South-Korea (Korea Republic). 


```python
df.loc[df["Home Team Name"].str.contains('Korea'), "Home Team Name" ]
```

Imagine that for some reason, we simply want Korea listed as one entry, so we want to replace every "Home Team Name" and "Away Team Name" entry that contains "Korea" to simply "Korea". In the same way, we want to change the columns "Home Team Initials" and "Away Team Initials" to NSK (North & South Korea) instead of "KOR" and "PRK". 


```python

```

Make sure to verify your answer!


```python

```

## Summary

In this lab, you learned how to access data within Pandas!
