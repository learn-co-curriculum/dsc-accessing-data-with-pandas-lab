# Accessing Data within Pandas - Lab

## Introduction

In this lab, we'll look at a dataset which contains information on World Cup matches. Let's use the pandas commands learned in the previous lesson to learn more about our data!

## Objectives

You will be able to: 

- Use pandas methods and attributes to access information about a dataset 
- Index pandas dataframes with .loc, .iloc, and column names 
- Use a boolean mask to index pandas series and dataframes

## Load the Data

Load the file `'WorldCupMatches.csv'` as a DataFrame in pandas.


```python
# Import pandas using the standard alias
import pandas as pd

# Load 'WorldCupMatches.csv' as a DataFrame
df = pd.read_csv('WorldCupMatches.csv')
```

## Common Methods and Attributes

Use the correct method to display the **first 7 rows** of the dataset.


```python
# Display the first 7 rows of df
df.head(7)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Datetime</th>
      <th>Stage</th>
      <th>Stadium</th>
      <th>City</th>
      <th>Home Team Name</th>
      <th>Home Team Goals</th>
      <th>Away Team Goals</th>
      <th>Away Team Name</th>
      <th>Win conditions</th>
      <th>Attendance</th>
      <th>Half-time Home Goals</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1930</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 1</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>France</td>
      <td>4</td>
      <td>1</td>
      <td>Mexico</td>
      <td></td>
      <td>4444.0</td>
      <td>3</td>
      <td>0</td>
      <td>LOMBARDI Domingo (URU)</td>
      <td>CRISTOPHE Henry (BEL)</td>
      <td>REGO Gilberto (BRA)</td>
      <td>201</td>
      <td>1096</td>
      <td>FRA</td>
      <td>MEX</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1930</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 4</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>USA</td>
      <td>3</td>
      <td>0</td>
      <td>Belgium</td>
      <td></td>
      <td>18346.0</td>
      <td>2</td>
      <td>0</td>
      <td>MACIAS Jose (ARG)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>201</td>
      <td>1090</td>
      <td>USA</td>
      <td>BEL</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1930</td>
      <td>14 Jul 1930 - 12:45</td>
      <td>Group 2</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Yugoslavia</td>
      <td>2</td>
      <td>1</td>
      <td>Brazil</td>
      <td></td>
      <td>24059.0</td>
      <td>2</td>
      <td>0</td>
      <td>TEJADA Anibal (URU)</td>
      <td>VALLARINO Ricardo (URU)</td>
      <td>BALWAY Thomas (FRA)</td>
      <td>201</td>
      <td>1093</td>
      <td>YUG</td>
      <td>BRA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1930</td>
      <td>14 Jul 1930 - 14:50</td>
      <td>Group 3</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>Romania</td>
      <td>3</td>
      <td>1</td>
      <td>Peru</td>
      <td></td>
      <td>2549.0</td>
      <td>1</td>
      <td>0</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>201</td>
      <td>1098</td>
      <td>ROU</td>
      <td>PER</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1930</td>
      <td>15 Jul 1930 - 16:00</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Argentina</td>
      <td>1</td>
      <td>0</td>
      <td>France</td>
      <td></td>
      <td>23409.0</td>
      <td>0</td>
      <td>0</td>
      <td>REGO Gilberto (BRA)</td>
      <td>SAUCEDO Ulises (BOL)</td>
      <td>RADULESCU Constantin (ROU)</td>
      <td>201</td>
      <td>1085</td>
      <td>ARG</td>
      <td>FRA</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1930</td>
      <td>16 Jul 1930 - 14:45</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Chile</td>
      <td>3</td>
      <td>0</td>
      <td>Mexico</td>
      <td></td>
      <td>9249.0</td>
      <td>1</td>
      <td>0</td>
      <td>CRISTOPHE Henry (BEL)</td>
      <td>APHESTEGUY Martin (URU)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>201</td>
      <td>1095</td>
      <td>CHI</td>
      <td>MEX</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1930</td>
      <td>17 Jul 1930 - 12:45</td>
      <td>Group 2</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Yugoslavia</td>
      <td>4</td>
      <td>0</td>
      <td>Bolivia</td>
      <td></td>
      <td>18306.0</td>
      <td>0</td>
      <td>0</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>LOMBARDI Domingo (URU)</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>201</td>
      <td>1092</td>
      <td>YUG</td>
      <td>BOL</td>
    </tr>
  </tbody>
</table>
</div>



Display the **last 3 rows** of the dataset.


```python
# Display the last 3 rows of df
df.tail(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Datetime</th>
      <th>Stage</th>
      <th>Stadium</th>
      <th>City</th>
      <th>Home Team Name</th>
      <th>Home Team Goals</th>
      <th>Away Team Goals</th>
      <th>Away Team Name</th>
      <th>Win conditions</th>
      <th>Attendance</th>
      <th>Half-time Home Goals</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>849</th>
      <td>2014</td>
      <td>09 Jul 2014 - 17:00</td>
      <td>Semi-finals</td>
      <td>Arena de Sao Paulo</td>
      <td>Sao Paulo</td>
      <td>Netherlands</td>
      <td>0</td>
      <td>0</td>
      <td>Argentina</td>
      <td>Argentina win on penalties (2 - 4)</td>
      <td>63267.0</td>
      <td>0</td>
      <td>0</td>
      <td>C�neyt �AKIR (TUR)</td>
      <td>DURAN Bahattin (TUR)</td>
      <td>ONGUN Tarik (TUR)</td>
      <td>255955</td>
      <td>300186490</td>
      <td>NED</td>
      <td>ARG</td>
    </tr>
    <tr>
      <th>850</th>
      <td>2014</td>
      <td>12 Jul 2014 - 17:00</td>
      <td>Play-off for third place</td>
      <td>Estadio Nacional</td>
      <td>Brasilia</td>
      <td>Brazil</td>
      <td>0</td>
      <td>3</td>
      <td>Netherlands</td>
      <td></td>
      <td>68034.0</td>
      <td>0</td>
      <td>2</td>
      <td>HAIMOUDI Djamel (ALG)</td>
      <td>ACHIK Redouane (MAR)</td>
      <td>ETCHIALI Abdelhak (ALG)</td>
      <td>255957</td>
      <td>300186502</td>
      <td>BRA</td>
      <td>NED</td>
    </tr>
    <tr>
      <th>851</th>
      <td>2014</td>
      <td>13 Jul 2014 - 16:00</td>
      <td>Final</td>
      <td>Estadio do Maracana</td>
      <td>Rio De Janeiro</td>
      <td>Germany</td>
      <td>1</td>
      <td>0</td>
      <td>Argentina</td>
      <td>Germany win after extra time</td>
      <td>74738.0</td>
      <td>0</td>
      <td>0</td>
      <td>Nicola RIZZOLI (ITA)</td>
      <td>Renato FAVERANI (ITA)</td>
      <td>Andrea STEFANI (ITA)</td>
      <td>255959</td>
      <td>300186501</td>
      <td>GER</td>
      <td>ARG</td>
    </tr>
  </tbody>
</table>
</div>



Get a concise summary of the data using `.info()`. 


```python
# Print a concise summary of df
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 852 entries, 0 to 851
    Data columns (total 20 columns):
     #   Column                Non-Null Count  Dtype  
    ---  ------                --------------  -----  
     0   Year                  852 non-null    int64  
     1   Datetime              852 non-null    object 
     2   Stage                 852 non-null    object 
     3   Stadium               852 non-null    object 
     4   City                  852 non-null    object 
     5   Home Team Name        852 non-null    object 
     6   Home Team Goals       852 non-null    int64  
     7   Away Team Goals       852 non-null    int64  
     8   Away Team Name        852 non-null    object 
     9   Win conditions        852 non-null    object 
     10  Attendance            850 non-null    float64
     11  Half-time Home Goals  852 non-null    int64  
     12  Half-time Away Goals  852 non-null    int64  
     13  Referee               852 non-null    object 
     14  Assistant 1           852 non-null    object 
     15  Assistant 2           852 non-null    object 
     16  RoundID               852 non-null    int64  
     17  MatchID               852 non-null    int64  
     18  Home Team Initials    852 non-null    object 
     19  Away Team Initials    852 non-null    object 
    dtypes: float64(1), int64(7), object(12)
    memory usage: 133.2+ KB


Obtain a tuple representing the **number of rows and number of columns**.


```python
# Display the number of rows and columns in df
df.shape
```




    (852, 20)



Use the appropriate attribute to get the **column names**.


```python
# Display the column names of df
df.columns
```




    Index(['Year', 'Datetime', 'Stage', 'Stadium', 'City', 'Home Team Name',
           'Home Team Goals', 'Away Team Goals', 'Away Team Name',
           'Win conditions', 'Attendance', 'Half-time Home Goals',
           'Half-time Away Goals', 'Referee', 'Assistant 1', 'Assistant 2',
           'RoundID', 'MatchID', 'Home Team Initials', 'Away Team Initials'],
          dtype='object')



## Selecting DataFrame Information

When looking at the DataFrame's `.head()` and `.tail()`, you might have noticed that the games are structured chronologically in the DataFrame.

Use the right selection method to display all the information from the 3rd to the 5th game (i.e. **select rows 3 through 5 inclusive**).


```python
# Display rows 3 through 5
# .iloc interval is "half open", does not include 6 in the output
df.iloc[3:6]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Datetime</th>
      <th>Stage</th>
      <th>Stadium</th>
      <th>City</th>
      <th>Home Team Name</th>
      <th>Home Team Goals</th>
      <th>Away Team Goals</th>
      <th>Away Team Name</th>
      <th>Win conditions</th>
      <th>Attendance</th>
      <th>Half-time Home Goals</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>1930</td>
      <td>14 Jul 1930 - 14:50</td>
      <td>Group 3</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>Romania</td>
      <td>3</td>
      <td>1</td>
      <td>Peru</td>
      <td></td>
      <td>2549.0</td>
      <td>1</td>
      <td>0</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>201</td>
      <td>1098</td>
      <td>ROU</td>
      <td>PER</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1930</td>
      <td>15 Jul 1930 - 16:00</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Argentina</td>
      <td>1</td>
      <td>0</td>
      <td>France</td>
      <td></td>
      <td>23409.0</td>
      <td>0</td>
      <td>0</td>
      <td>REGO Gilberto (BRA)</td>
      <td>SAUCEDO Ulises (BOL)</td>
      <td>RADULESCU Constantin (ROU)</td>
      <td>201</td>
      <td>1085</td>
      <td>ARG</td>
      <td>FRA</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1930</td>
      <td>16 Jul 1930 - 14:45</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Chile</td>
      <td>3</td>
      <td>0</td>
      <td>Mexico</td>
      <td></td>
      <td>9249.0</td>
      <td>1</td>
      <td>0</td>
      <td>CRISTOPHE Henry (BEL)</td>
      <td>APHESTEGUY Martin (URU)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>201</td>
      <td>1095</td>
      <td>CHI</td>
      <td>MEX</td>
    </tr>
  </tbody>
</table>
</div>



Now, display the info from **game 5-9** (inclusive), but **only the `"Home Team Name"` and the `"Away Team Name"` columns**.


```python
# Display rows 5 through 9 and columns 'Home Team Name' and 'Away Team Name'
# .loc interval is not "half open", it includes the endpoint
df.loc[5:9, ['Home Team Name', 'Away Team Name']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Home Team Name</th>
      <th>Away Team Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>Chile</td>
      <td>Mexico</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Yugoslavia</td>
      <td>Bolivia</td>
    </tr>
    <tr>
      <th>7</th>
      <td>USA</td>
      <td>Paraguay</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Uruguay</td>
      <td>Peru</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Chile</td>
      <td>France</td>
    </tr>
  </tbody>
</table>
</div>



Next, we'd like the information on all the games played in **Group 3** for the **1950** World Cup.

Hint: You can combine conditions like this:

`df[(condition1) | (condition2)]`  -> Returns rows where either condition is true

`df[(condition1) & (condition2)]`  -> Returns rows where both conditions are true


```python
# Display all info for games played in 1950 for Group 3
# This time we don't need .loc because we are applying a
# boolean mask and our indexing uses rows only (all
# columns are selected)
df[(df["Year"] == 1950) & (df["Stage"] == "Group 3")]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Datetime</th>
      <th>Stage</th>
      <th>Stadium</th>
      <th>City</th>
      <th>Home Team Name</th>
      <th>Home Team Goals</th>
      <th>Away Team Goals</th>
      <th>Away Team Name</th>
      <th>Win conditions</th>
      <th>Attendance</th>
      <th>Half-time Home Goals</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>56</th>
      <td>1950</td>
      <td>25 Jun 1950 - 15:00</td>
      <td>Group 3</td>
      <td>Pacaembu</td>
      <td>Sao Paulo</td>
      <td>Sweden</td>
      <td>3</td>
      <td>2</td>
      <td>Italy</td>
      <td></td>
      <td>36502.0</td>
      <td>2</td>
      <td>1</td>
      <td>LUTZ Jean (SUI)</td>
      <td>BERANEK Alois (AUT)</td>
      <td>TEJADA Carlos (MEX)</td>
      <td>208</td>
      <td>1219</td>
      <td>SWE</td>
      <td>ITA</td>
    </tr>
    <tr>
      <th>61</th>
      <td>1950</td>
      <td>29 Jun 1950 - 15:30</td>
      <td>Group 3</td>
      <td>Durival de Brito</td>
      <td>Curitiba</td>
      <td>Sweden</td>
      <td>2</td>
      <td>2</td>
      <td>Paraguay</td>
      <td></td>
      <td>7903.0</td>
      <td>2</td>
      <td>1</td>
      <td>MITCHELL Robert (SCO)</td>
      <td>LEMESIC Leo (YUG)</td>
      <td>GARCIA Prudencio (USA)</td>
      <td>208</td>
      <td>1228</td>
      <td>SWE</td>
      <td>PAR</td>
    </tr>
    <tr>
      <th>65</th>
      <td>1950</td>
      <td>02 Jul 1950 - 15:00</td>
      <td>Group 3</td>
      <td>Pacaembu</td>
      <td>Sao Paulo</td>
      <td>Italy</td>
      <td>2</td>
      <td>0</td>
      <td>Paraguay</td>
      <td></td>
      <td>25811.0</td>
      <td>1</td>
      <td>0</td>
      <td>ELLIS Arthur (ENG)</td>
      <td>GARCIA Prudencio (USA)</td>
      <td>DE LA SALLE Charles (FRA)</td>
      <td>208</td>
      <td>1218</td>
      <td>ITA</td>
      <td>PAR</td>
    </tr>
  </tbody>
</table>
</div>



Let's repeat the command above, but this time display **only the attendance column** for the Group 3 games. 


```python
# Print the 'Attendance' column for games played in 1950
# for Group 3
# This time we want to use df.loc instead of just
# df[boolean mask] in order to select certain rows AND
# certain columns
df.loc[(df['Year'] == 1950) & (df['Stage'] == 'Group 3'), 'Attendance']
```




    56    36502.0
    61     7903.0
    65    25811.0
    Name: Attendance, dtype: float64



Throughout the entire history of the World Cup as recorded in this dataset, **how many home games were played by the Netherlands**?

(Remember that you can use the `len()` built-in function to find the number of rows in a DataFrame.)


```python
# Number of home games played by the Netherlands
# Here we are just using df[boolean mask] again
neth_home = len(df[df['Home Team Name'] == ('Netherlands')])
neth_home
```




    32



**How many games were played by the Netherlands in total**?


```python
# Number of games played by the Netherlands in total
# Conveniently we already saved neth_home as a variable
# so we just need to find the number of times they were
# the away team and sum them
len(df[df['Away Team Name']==('Netherlands')]) + neth_home
```




    54



Next, let's try and figure out **how many games the USA played in the 2014 World Cup**.


```python

# Number of games the USA played in the 2014 world cup

# Mask will return True or False for each row of df
usa_2014_mask = (
    # USA is home team OR away team
    (
        (df['Home Team Name'] == 'USA') |
        (df['Away Team Name'] == 'USA')
    ) &
    # AND year is 2014
    (df['Year'] == 2014)
)

# Filter df using mask and find its length
len(df[usa_2014_mask])
```




    5



Now, let's try to find out **how many countries participated in the 1986 World Cup**.

Hint 1: As a first step, create a new dataset that only contains games in that year.

Hint 2: Make sure you don't end up with duplicate country names. Consider using `set()` or `.unique()`.


```python
# Number of countries participated in the 1986 world cup

# Copy of dataset that is limited to 1986, and only team name cols
games_86 = df.loc[df['Year'] == 1986, ['Home Team Name', 'Away Team Name']].copy()
print("Total games in 1986:", len(games_86))
print()

# Converting to Python set approach (some base Python)
# Create sets of unique home and away teams
home = set(games_86['Home Team Name'])
away = set(games_86['Away Team Name'])
# Get the length of the union of those sets
print("Unique countries participating:", len(home | away))

# Melt approach (all pandas)
# Use `melt` to stack home and away variables on top of each other
# This creates one column "Home or Away" with values of either "Home
# Team Name" or "Away Team Name", one column "Team" with the team name
teams_86 = games_86.melt(var_name = "Home or Away", value_name="Team")
# Find unique number of teams using "Team" column
print("Unique countries participating:", len(teams_86["Team"].unique()))
```

    Total games in 1986: 52
    
    Unique countries participating: 24
    Unique countries participating: 24


## Changing Values and Creating New Columns

In World Cup history, **how many matches had 5 goals or more in total**? Create a column `"Total Goals"` to answer this question.


```python
# Number of matches that had more than 5 goals in total

# New column created by summing the other two
# We don't need a loop because pandas will automatically create
# one and "broadcast" each value from the columns being summed
df['Total Goals'] = df['Home Team Goals'] + df['Away Team Goals']
# Length of df where the new column >= 5
len(df[df['Total Goals'] >= 5])
```




    147



Now **create a new column `"Half-time Goals"`** in `df` that includes both home and away values.


```python
# Create a new column 'Half-time Goals' in df
df['Half-time Goals'] = df['Half-time Home Goals'] + df['Half-time Away Goals']
df.columns
```




    Index(['Year', 'Datetime', 'Stage', 'Stadium', 'City', 'Home Team Name',
           'Home Team Goals', 'Away Team Goals', 'Away Team Name',
           'Win conditions', 'Attendance', 'Half-time Home Goals',
           'Half-time Away Goals', 'Referee', 'Assistant 1', 'Assistant 2',
           'RoundID', 'MatchID', 'Home Team Initials', 'Away Team Initials',
           'Total Goals', 'Half-time Goals'],
          dtype='object')



Run the code below. You'll notice that for Korea, there are records for both North-Korea (Korea DPR) and South-Korea (Korea Republic). 


```python
# Print all records containing the string 'Korea'
df.loc[df['Home Team Name'].str.contains('Korea'), 'Home Team Name']
```




    179         Korea DPR
    187         Korea DPR
    374    Korea Republic
    386    Korea Republic
    434    Korea Republic
    444    Korea Republic
    480    Korea Republic
    524    Korea Republic
    593    Korea Republic
    609    Korea Republic
    635    Korea Republic
    642    Korea Republic
    655    Korea Republic
    710    Korea Republic
    753         Korea DPR
    802    Korea Republic
    818    Korea Republic
    Name: Home Team Name, dtype: object



Imagine that, for some reason, we simply want Korea listed as one entry, so we want to replace every "Home Team Name" and "Away Team Name" entry that contains "Korea" to simply "Korea". In the same way, we want to change the columns "Home Team Initials" and "Away Team Initials" to NSK (North & South Korea) instead of "KOR" and "PRK". 


```python
# Update the 'Home Team Name' and 'Home Team Initials' columns 

korea_names = ['Korea DPR', 'Korea Republic']
korea_initials = ['KOR', 'PRK']

# Home team name
df.loc[df['Home Team Name'].isin(korea_names), 'Home Team Name'] = 'Korea'
# Away team name
df.loc[df['Away Team Name'].isin(korea_names), 'Away Team Name'] = 'Korea'
# Home team initials
df.loc[df['Home Team Initials'].isin(korea_initials), 'Home Team Initials'] = 'NSK'
# Away team initials
df.loc[df['Away Team Initials'].isin(korea_initials), 'Away Team Initials'] = 'NSK'
```

Make sure to verify your answer!


```python
# Check the updated columns

korea_mask = (
    (df['Home Team Name'].str.contains('Korea')) |
    (df['Away Team Name'].str.contains('Korea'))
)

df.loc[korea_mask, ['Home Team Name', 'Away Team Name', 'Home Team Initials', 'Away Team Initials']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Home Team Name</th>
      <th>Away Team Name</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>80</th>
      <td>Hungary</td>
      <td>Korea</td>
      <td>HUN</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Turkey</td>
      <td>Korea</td>
      <td>TUR</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>171</th>
      <td>Soviet Union</td>
      <td>Korea</td>
      <td>URS</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>179</th>
      <td>Korea</td>
      <td>Chile</td>
      <td>NSK</td>
      <td>CHI</td>
    </tr>
    <tr>
      <th>187</th>
      <td>Korea</td>
      <td>Italy</td>
      <td>NSK</td>
      <td>ITA</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Portugal</td>
      <td>Korea</td>
      <td>POR</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>364</th>
      <td>Argentina</td>
      <td>Korea</td>
      <td>ARG</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>374</th>
      <td>Korea</td>
      <td>Bulgaria</td>
      <td>NSK</td>
      <td>BUL</td>
    </tr>
    <tr>
      <th>386</th>
      <td>Korea</td>
      <td>Italy</td>
      <td>NSK</td>
      <td>ITA</td>
    </tr>
    <tr>
      <th>421</th>
      <td>Belgium</td>
      <td>Korea</td>
      <td>BEL</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>434</th>
      <td>Korea</td>
      <td>Spain</td>
      <td>NSK</td>
      <td>ESP</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Korea</td>
      <td>Uruguay</td>
      <td>NSK</td>
      <td>URU</td>
    </tr>
    <tr>
      <th>464</th>
      <td>Spain</td>
      <td>Korea</td>
      <td>ESP</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>480</th>
      <td>Korea</td>
      <td>Bolivia</td>
      <td>NSK</td>
      <td>BOL</td>
    </tr>
    <tr>
      <th>490</th>
      <td>Germany</td>
      <td>Korea</td>
      <td>GER</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>524</th>
      <td>Korea</td>
      <td>Mexico</td>
      <td>NSK</td>
      <td>MEX</td>
    </tr>
    <tr>
      <th>542</th>
      <td>Netherlands</td>
      <td>Korea</td>
      <td>NED</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>556</th>
      <td>Belgium</td>
      <td>Korea</td>
      <td>BEL</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>593</th>
      <td>Korea</td>
      <td>Poland</td>
      <td>NSK</td>
      <td>POL</td>
    </tr>
    <tr>
      <th>609</th>
      <td>Korea</td>
      <td>USA</td>
      <td>NSK</td>
      <td>USA</td>
    </tr>
    <tr>
      <th>625</th>
      <td>Portugal</td>
      <td>Korea</td>
      <td>POR</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>635</th>
      <td>Korea</td>
      <td>Italy</td>
      <td>NSK</td>
      <td>ITA</td>
    </tr>
    <tr>
      <th>639</th>
      <td>Spain</td>
      <td>Korea</td>
      <td>ESP</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>640</th>
      <td>Germany</td>
      <td>Korea</td>
      <td>GER</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>642</th>
      <td>Korea</td>
      <td>Turkey</td>
      <td>NSK</td>
      <td>TUR</td>
    </tr>
    <tr>
      <th>655</th>
      <td>Korea</td>
      <td>Togo</td>
      <td>NSK</td>
      <td>TOG</td>
    </tr>
    <tr>
      <th>672</th>
      <td>France</td>
      <td>Korea</td>
      <td>FRA</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>691</th>
      <td>Switzerland</td>
      <td>Korea</td>
      <td>SUI</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>710</th>
      <td>Korea</td>
      <td>Greece</td>
      <td>NSK</td>
      <td>GRE</td>
    </tr>
    <tr>
      <th>721</th>
      <td>Brazil</td>
      <td>Korea</td>
      <td>BRA</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>725</th>
      <td>Argentina</td>
      <td>Korea</td>
      <td>ARG</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>737</th>
      <td>Portugal</td>
      <td>Korea</td>
      <td>POR</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>742</th>
      <td>Nigeria</td>
      <td>Korea</td>
      <td>NGA</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>753</th>
      <td>Korea</td>
      <td>C�te d'Ivoire</td>
      <td>NSK</td>
      <td>CIV</td>
    </tr>
    <tr>
      <th>756</th>
      <td>Uruguay</td>
      <td>Korea</td>
      <td>URU</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>788</th>
      <td>Russia</td>
      <td>Korea</td>
      <td>RUS</td>
      <td>NSK</td>
    </tr>
    <tr>
      <th>802</th>
      <td>Korea</td>
      <td>Algeria</td>
      <td>NSK</td>
      <td>ALG</td>
    </tr>
    <tr>
      <th>818</th>
      <td>Korea</td>
      <td>Belgium</td>
      <td>NSK</td>
      <td>BEL</td>
    </tr>
  </tbody>
</table>
</div>



## Summary

In this lab, you practiced accessing data within Pandas!
