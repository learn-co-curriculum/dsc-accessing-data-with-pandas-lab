
# World Cup Matches

### Load the WorldCupMatches.csv file as a pandas dataframe.


```python
import pandas as pd
df = pd.read_csv('WorldCupMatches.csv')
print(len(df))
df.head()
```

    4572





<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
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
      <td>1930.0</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 1</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>France</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>Mexico</td>
      <td></td>
      <td>4444.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>LOMBARDI Domingo (URU)</td>
      <td>CRISTOPHE Henry (BEL)</td>
      <td>REGO Gilberto (BRA)</td>
      <td>201.0</td>
      <td>1096.0</td>
      <td>FRA</td>
      <td>MEX</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1930.0</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 4</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>USA</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>Belgium</td>
      <td></td>
      <td>18346.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>MACIAS Jose (ARG)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>201.0</td>
      <td>1090.0</td>
      <td>USA</td>
      <td>BEL</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1930.0</td>
      <td>14 Jul 1930 - 12:45</td>
      <td>Group 2</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Yugoslavia</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>Brazil</td>
      <td></td>
      <td>24059.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>TEJADA Anibal (URU)</td>
      <td>VALLARINO Ricardo (URU)</td>
      <td>BALWAY Thomas (FRA)</td>
      <td>201.0</td>
      <td>1093.0</td>
      <td>YUG</td>
      <td>BRA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1930.0</td>
      <td>14 Jul 1930 - 14:50</td>
      <td>Group 3</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>Romania</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>Peru</td>
      <td></td>
      <td>2549.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>201.0</td>
      <td>1098.0</td>
      <td>ROU</td>
      <td>PER</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1930.0</td>
      <td>15 Jul 1930 - 16:00</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Argentina</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>France</td>
      <td></td>
      <td>23409.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>REGO Gilberto (BRA)</td>
      <td>SAUCEDO Ulises (BOL)</td>
      <td>RADULESCU Constantin (ROU)</td>
      <td>201.0</td>
      <td>1085.0</td>
      <td>ARG</td>
      <td>FRA</td>
    </tr>
  </tbody>
</table>
</div>



### Subset the DataFrame to only rows where the Home Team Name is populated.


```python
tot = len(df)
df = df[~(df['Home Team Name'].isnull())]
print(len(df))
print('Percent remaining: {}%'.format(round(len(df)/tot, 4)*100))
df.head()
```

    852
    Percent remaining: 18.64%





<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
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
      <td>1930.0</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 1</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>France</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>Mexico</td>
      <td></td>
      <td>4444.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>LOMBARDI Domingo (URU)</td>
      <td>CRISTOPHE Henry (BEL)</td>
      <td>REGO Gilberto (BRA)</td>
      <td>201.0</td>
      <td>1096.0</td>
      <td>FRA</td>
      <td>MEX</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1930.0</td>
      <td>13 Jul 1930 - 15:00</td>
      <td>Group 4</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>USA</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>Belgium</td>
      <td></td>
      <td>18346.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>MACIAS Jose (ARG)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>201.0</td>
      <td>1090.0</td>
      <td>USA</td>
      <td>BEL</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1930.0</td>
      <td>14 Jul 1930 - 12:45</td>
      <td>Group 2</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Yugoslavia</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>Brazil</td>
      <td></td>
      <td>24059.0</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>TEJADA Anibal (URU)</td>
      <td>VALLARINO Ricardo (URU)</td>
      <td>BALWAY Thomas (FRA)</td>
      <td>201.0</td>
      <td>1093.0</td>
      <td>YUG</td>
      <td>BRA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1930.0</td>
      <td>14 Jul 1930 - 14:50</td>
      <td>Group 3</td>
      <td>Pocitos</td>
      <td>Montevideo</td>
      <td>Romania</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>Peru</td>
      <td></td>
      <td>2549.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>WARNKEN Alberto (CHI)</td>
      <td>LANGENUS Jean (BEL)</td>
      <td>MATEUCCI Francisco (URU)</td>
      <td>201.0</td>
      <td>1098.0</td>
      <td>ROU</td>
      <td>PER</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1930.0</td>
      <td>15 Jul 1930 - 16:00</td>
      <td>Group 1</td>
      <td>Parque Central</td>
      <td>Montevideo</td>
      <td>Argentina</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>France</td>
      <td></td>
      <td>23409.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>REGO Gilberto (BRA)</td>
      <td>SAUCEDO Ulises (BOL)</td>
      <td>RADULESCU Constantin (ROU)</td>
      <td>201.0</td>
      <td>1085.0</td>
      <td>ARG</td>
      <td>FRA</td>
    </tr>
  </tbody>
</table>
</div>



### How many of the matches were in Montevideo?


```python
temp = df[df['City'].str.contains('Montevideo')]
print(len(temp))
```

    18


###  How many matches were played where the home team's name contained a (capital) 'M'?


```python
temp = df[df['City'].str.contains('M')]
print(len(temp))
```

    152


### How many matches did USA play in 2014?  

Hint: they could have been home or away.  

You can combine conditions like this:  
df[(condition1) | (condition2)] #Returns rows where either condition is true  
df[(condition1) & (condition2)] #Returns rows where both conditions are true  


```python
temp = df[(df.Year==2014)
         & ((df['Home Team Name'] == 'USA') | (df['Away Team Name']=='USA'))
         ]
print(len(temp))
```

    5


### How many teams played in 1986?


```python
temp = df[df.Year==1986]
home = list(temp['Home Team Name'].unique())
away = list(temp['Away Team Name'].unique())
print(len(home))
home += away
print(len(home))
print(len(set(home)))
```

    24
    48
    24


### How many matches were there with 5 or more total goals?


```python
df['Total_Goals'] = df['Home Team Goals'] + df['Away Team Goals']
print(len(df[df.Total_Goals>=5]))
```

    147

