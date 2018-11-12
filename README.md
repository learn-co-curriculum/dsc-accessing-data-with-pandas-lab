
# World Cup Matches

In this lab, we'll look at a data set which contains information World cup matches. Let's use the pandas commands learned in the previous lecture to learn more about our data!

## Load the data

Load the file `WorldCupMatches.csv` as a dataframe in Pandas


```python
import pandas as pd
df = pd.read_csv('WorldCupMatches.csv')
```

## Common methods and attributes

Use the correct method to look at the first 7 rows of the data set.


```python
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



Look at the last 3 rows of the data set.


```python
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



Get a concise summary of your data using `.info()`


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 852 entries, 0 to 851
    Data columns (total 20 columns):
    Year                    852 non-null int64
    Datetime                852 non-null object
    Stage                   852 non-null object
    Stadium                 852 non-null object
    City                    852 non-null object
    Home Team Name          852 non-null object
    Home Team Goals         852 non-null int64
    Away Team Goals         852 non-null int64
    Away Team Name          852 non-null object
    Win conditions          852 non-null object
    Attendance              850 non-null float64
    Half-time Home Goals    852 non-null int64
    Half-time Away Goals    852 non-null int64
    Referee                 852 non-null object
    Assistant 1             852 non-null object
    Assistant 2             852 non-null object
    RoundID                 852 non-null int64
    MatchID                 852 non-null int64
    Home Team Initials      852 non-null object
    Away Team Initials      852 non-null object
    dtypes: float64(1), int64(7), object(12)
    memory usage: 133.2+ KB


Obtain a tuple representing the number of rows and number of columns


```python
df.shape
```




    (852, 20)



Use the appropriate attribute to get the column names


```python
df.columns
```




    Index(['Year', 'Datetime', 'Stage', 'Stadium', 'City', 'Home Team Name',
           'Home Team Goals', 'Away Team Goals', 'Away Team Name',
           'Win conditions', 'Attendance', 'Half-time Home Goals',
           'Half-time Away Goals', 'Referee', 'Assistant 1', 'Assistant 2',
           'RoundID', 'MatchID', 'Home Team Initials', 'Away Team Initials'],
          dtype='object')



## Selecting dataframe information

When looking at the dataframe's `.head()`, you might have noticed that the games are structured chronologically in the dataframe.

Use the right selection method to print all the information from the 3rd to the 5th game.


```python
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



Now, print all the info from game 5-8, but we're only interested to print out the "Home Team Name" and the "Away Team Name", 


```python
df.loc[5:9,["Home Team Name", "Away Team Name"]]
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



Next, we'd like the information on all the games played in Group 3 for the 1950 World Cup.


```python
df.loc[(df["Year"] == 1950) & (df["Stage"]=="Group 3")]
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



Let's repeat the command above, but now we only want to print out the attendance column for the Group 3 games

You can combine conditions like this:

`df[(condition1) | (condition2)]`  -> Returns rows where either condition is true

`df[(condition1) & (condition2)]`  -> Returns rows where both conditions are true


```python
df.loc[(df["Year"] == 1950) & (df["Stage"]=="Group 3"), "Attendance"]
```




    56    36502.0
    61     7903.0
    65    25811.0
    Name: Attendance, dtype: float64



Throughout the entire history of the world cup, How many Home games were played by the Netherlands?


```python
Neth_home = df[df['Home Team Name']==('Netherlands')]
print(len(Neth_home))
```

    32


How many games were played by the Netherlands in total?


```python
Neth_away = df[df['Away Team Name']==('Netherlands')]
print(len(Neth_home)+len(Neth_away))
```

    54


Next, let's try and figure out how many games the USA played in the 2014 world cup. 


```python
USA_home_and_away = df[(df.Year==2014)
         & ((df['Home Team Name'] == 'USA') | (df['Away Team Name']=='USA'))
         ]
print(len(USA_home_and_away))
```

    5


Now, let's try to find out how many countries participated in the 1986 world cup.

Hint 1: as a first step, create a new data set that only contain games in that year.

Hint 2: You can use `.unique()` to make sure you don't end up with duplicate country names.


```python
games_86 = df[df.Year==1986]
home = list(games_86['Home Team Name'].unique())
away = list(games_86['Away Team Name'].unique())
print(len(home))
home += away
print(len(home))
print(len(set(home)))
```

    24
    48
    24


In the world cup history, how matches had more than 5 goals in total?


```python
df['Total_Goals'] = df['Home Team Goals'] + df['Away Team Goals']
print(len(df[df.Total_Goals>=5]))
```

    147


## Changing values and creating new columns

With the information you currently have in your `df`, create a new column "Half-time Goals".


```python
df["Half-time Goals"] = df["Half-time Home Goals"] + df["Half-time Away Goals"]
```

Run the code below. You'll notice that for Korea, there are records for both North-Korea (Korea DPR) and South-Korea (Korea Republic). 


```python
df.loc[df["Home Team Name"].str.contains('Korea'), "Home Team Name" ]
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



Imagine that for some reason, we simply want Korea listed as one entry, so we want to replace every "Home Team Name" and "Away Team Name" entry that contains "Korea" to simply "Korea". In the same way, we want to change the columns "Home Team Initials" and "Away Team Initials" to NSK (North & South Korea) instead of "KOR" and "PRK". 


```python
df.loc[df["Home Team Name"] == "Korea DPR", "Home Team Name"] = "Korea"
df.loc[df["Home Team Name"] == "Korea Republic", "Home Team Name"] = "Korea"
df.loc[df["Away Team Name"] == "Korea DPR", "Away Team Name"] = "Korea"
df.loc[df["Away Team Name"] == "Korea Republic", "Away Team Name"] = "Korea"
df.loc[df["Home Team Initials"] == "KOR", "Home Team Initials"] = "NSK"
df.loc[df["Home Team Initials"] == "KOR", "Home Team Initials"] = "NSK"
df.loc[df["Away Team Initials"] == "PRK", "Away Team Initials"] = "NSK"
df.loc[df["Away Team Initials"] == "PRK", "Away Team Initials"] = "NSK"
```

Make sure to verify your answer!


```python
df.loc[df["Home Team Name"].str.contains('Korea')]
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
      <th>...</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
      <th>Total_Goals</th>
      <th>Half-time Goals</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>179</th>
      <td>1966</td>
      <td>15 Jul 1966 - 19:30</td>
      <td>Group 4</td>
      <td>Ayresome Park</td>
      <td>Middlesbrough</td>
      <td>Korea</td>
      <td>1</td>
      <td>1</td>
      <td>Chile</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>KANDIL Aly Hussein (EGY)</td>
      <td>CRAWFORD William (SCO)</td>
      <td>FINNEY Jim (ENG)</td>
      <td>238</td>
      <td>1609</td>
      <td>PRK</td>
      <td>CHI</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>187</th>
      <td>1966</td>
      <td>19 Jul 1966 - 19:30</td>
      <td>Group 4</td>
      <td>Ayresome Park</td>
      <td>Middlesbrough</td>
      <td>Korea</td>
      <td>1</td>
      <td>0</td>
      <td>Italy</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>SCHWINTE Pierre (FRA)</td>
      <td>ADAIR John (NIR)</td>
      <td>TAYLOR John (ENG)</td>
      <td>238</td>
      <td>1679</td>
      <td>PRK</td>
      <td>ITA</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>374</th>
      <td>1986</td>
      <td>05 Jun 1986 - 16:00</td>
      <td>Group A</td>
      <td>Estadio Ol�mpico Universitario</td>
      <td>Mexico City</td>
      <td>Korea</td>
      <td>1</td>
      <td>1</td>
      <td>Bulgaria</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>AL SHANAR Fallaj Khuzam (KSA)</td>
      <td>IGNA Ioan (ROU)</td>
      <td>BUTENKO Valeri (RUS)</td>
      <td>308</td>
      <td>460</td>
      <td>NSK</td>
      <td>BUL</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>386</th>
      <td>1986</td>
      <td>10 Jun 1986 - 12:00</td>
      <td>Group A</td>
      <td>Cuauhtemoc</td>
      <td>Puebla</td>
      <td>Korea</td>
      <td>2</td>
      <td>3</td>
      <td>Italy</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>SOCHA David (USA)</td>
      <td>URREA Joaquin (MEX)</td>
      <td>AL SHARIF Jamal (SYR)</td>
      <td>308</td>
      <td>643</td>
      <td>NSK</td>
      <td>ITA</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>434</th>
      <td>1990</td>
      <td>17 Jun 1990 - 21:00</td>
      <td>Group E</td>
      <td>Dacia Arena</td>
      <td>Udine</td>
      <td>Korea</td>
      <td>1</td>
      <td>3</td>
      <td>Spain</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>JACOME GUERRERO Elias V. (ECU)</td>
      <td>MAGNI Pierluigi (ITA)</td>
      <td>LOUSTAU Juan (ARG)</td>
      <td>322</td>
      <td>175</td>
      <td>NSK</td>
      <td>ESP</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>444</th>
      <td>1990</td>
      <td>21 Jun 1990 - 17:00</td>
      <td>Group E</td>
      <td>Friuli</td>
      <td>Udine</td>
      <td>Korea</td>
      <td>0</td>
      <td>1</td>
      <td>Uruguay</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>LANESE Tullio (ITA)</td>
      <td>DIRAMBA Jean Fidele (GAB)</td>
      <td>JOUINI Neji (TUN)</td>
      <td>322</td>
      <td>290</td>
      <td>NSK</td>
      <td>URU</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>480</th>
      <td>1994</td>
      <td>23 Jun 1994 - 19:30</td>
      <td>Group C</td>
      <td>Foxboro Stadium</td>
      <td>Boston</td>
      <td>Korea</td>
      <td>0</td>
      <td>0</td>
      <td>Bolivia</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>MOTTRAM Leslie (SCO)</td>
      <td>MATTHYS Luc (BEL)</td>
      <td>EVERSTIG Mikael (SWE)</td>
      <td>337</td>
      <td>3065</td>
      <td>NSK</td>
      <td>BOL</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>524</th>
      <td>1998</td>
      <td>13 Jun 1998 - 17:30</td>
      <td>Group E</td>
      <td>Stade de Gerland</td>
      <td>Lyon</td>
      <td>Korea</td>
      <td>1</td>
      <td>3</td>
      <td>Mexico</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>BENKO Gunter (AUT)</td>
      <td>FRED Lencie (VAN)</td>
      <td>SCHNEIDER Erich (GER)</td>
      <td>1014</td>
      <td>8732</td>
      <td>NSK</td>
      <td>MEX</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>593</th>
      <td>2002</td>
      <td>04 Jun 2002 - 20:30</td>
      <td>Group D</td>
      <td>Busan Asiad Main Stadium</td>
      <td>Busan</td>
      <td>Korea</td>
      <td>2</td>
      <td>0</td>
      <td>Poland</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>RUIZ Oscar (COL)</td>
      <td>DORIRI Elise (VAN)</td>
      <td>LINDBERG Leif (SWE)</td>
      <td>43950100</td>
      <td>43950014</td>
      <td>NSK</td>
      <td>POL</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>609</th>
      <td>2002</td>
      <td>10 Jun 2002 - 15:30</td>
      <td>Group D</td>
      <td>Daegu World Cup Stadium</td>
      <td>Daegu</td>
      <td>Korea</td>
      <td>1</td>
      <td>1</td>
      <td>USA</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>MEIER Urs (SUI)</td>
      <td>BEREUTER Egon (AUT)</td>
      <td>TOMUSANGE Ali (UGA)</td>
      <td>43950100</td>
      <td>43950030</td>
      <td>NSK</td>
      <td>USA</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>635</th>
      <td>2002</td>
      <td>18 Jun 2002 - 20:30</td>
      <td>Round of 16</td>
      <td>Daejeon World Cup Stadium</td>
      <td>Daejeon</td>
      <td>Korea</td>
      <td>2</td>
      <td>1</td>
      <td>Italy</td>
      <td>Win on Golden Goal</td>
      <td>...</td>
      <td>0</td>
      <td>MORENO Byron (ECU)</td>
      <td>RATTALINO Jorge (ARG)</td>
      <td>SZEKELY Ferenc (HUN)</td>
      <td>43950200</td>
      <td>43950056</td>
      <td>NSK</td>
      <td>ITA</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>642</th>
      <td>2002</td>
      <td>29 Jun 2002 - 20:00</td>
      <td>Third place</td>
      <td>Daegu World Cup Stadium</td>
      <td>Daegu</td>
      <td>Korea</td>
      <td>2</td>
      <td>3</td>
      <td>Turkey</td>
      <td></td>
      <td>...</td>
      <td>3</td>
      <td>MANE Saad (KUW)</td>
      <td>ALTRAIFI Ali (KSA)</td>
      <td>VERGARA Hector (CAN)</td>
      <td>43950500</td>
      <td>43950063</td>
      <td>NSK</td>
      <td>TUR</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>655</th>
      <td>2006</td>
      <td>13 Jun 2006 - 15:00</td>
      <td>Group G</td>
      <td>FIFA World Cup Stadium, Frankfurt</td>
      <td>Frankfurt/Main</td>
      <td>Korea</td>
      <td>2</td>
      <td>1</td>
      <td>Togo</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>POLL Graham (ENG)</td>
      <td>SHARP Philip (ENG)</td>
      <td>TURNER Glenn (ENG)</td>
      <td>97410100</td>
      <td>97410014</td>
      <td>NSK</td>
      <td>TOG</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>710</th>
      <td>2010</td>
      <td>12 Jun 2010 - 13:30</td>
      <td>Group B</td>
      <td>Port Elizabeth Stadium</td>
      <td>Nelson Mandela Bay/Port Elizabeth</td>
      <td>Korea</td>
      <td>2</td>
      <td>0</td>
      <td>Greece</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>HESTER Michael (NZL)</td>
      <td>HINTZ Jan Hendrik (NZL)</td>
      <td>MAKASINI Tevita (TGA)</td>
      <td>249722</td>
      <td>300061459</td>
      <td>NSK</td>
      <td>GRE</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>753</th>
      <td>2010</td>
      <td>25 Jun 2010 - 16:00</td>
      <td>Group G</td>
      <td>Mbombela Stadium</td>
      <td>Nelspruit</td>
      <td>Korea</td>
      <td>0</td>
      <td>3</td>
      <td>C�te d'Ivoire</td>
      <td></td>
      <td>...</td>
      <td>2</td>
      <td>Alberto UNDIANO MALLENCO (ESP)</td>
      <td>MARTINEZ Fermin (ESP)</td>
      <td>YUSTE Juan (ESP)</td>
      <td>249722</td>
      <td>300061486</td>
      <td>PRK</td>
      <td>CIV</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>802</th>
      <td>2014</td>
      <td>22 Jun 2014 - 16:00</td>
      <td>Group H</td>
      <td>Estadio Beira-Rio</td>
      <td>Porto Alegre</td>
      <td>Korea</td>
      <td>2</td>
      <td>4</td>
      <td>Algeria</td>
      <td></td>
      <td>...</td>
      <td>3</td>
      <td>ROLDAN Wilmar (COL)</td>
      <td>DIAZ Eduardo (COL)</td>
      <td>LESCANO Christian (ECU)</td>
      <td>255931</td>
      <td>300186495</td>
      <td>NSK</td>
      <td>ALG</td>
      <td>6</td>
      <td>3</td>
    </tr>
    <tr>
      <th>818</th>
      <td>2014</td>
      <td>26 Jun 2014 - 17:00</td>
      <td>Group H</td>
      <td>Arena de Sao Paulo</td>
      <td>Sao Paulo</td>
      <td>Korea</td>
      <td>0</td>
      <td>1</td>
      <td>Belgium</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>Ben WILLIAMS (AUS)</td>
      <td>CREAM Matthew (AUS)</td>
      <td>ANAZ Hakan (AUS)</td>
      <td>255931</td>
      <td>300186480</td>
      <td>NSK</td>
      <td>BEL</td>
      <td>1</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>17 rows × 22 columns</p>
</div>




```python
df.loc[df["Away Team Name"].str.contains('Korea')]
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
      <th>...</th>
      <th>Half-time Away Goals</th>
      <th>Referee</th>
      <th>Assistant 1</th>
      <th>Assistant 2</th>
      <th>RoundID</th>
      <th>MatchID</th>
      <th>Home Team Initials</th>
      <th>Away Team Initials</th>
      <th>Total_Goals</th>
      <th>Half-time Goals</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>80</th>
      <td>1954</td>
      <td>17 Jun 1954 - 18:00</td>
      <td>Group 2</td>
      <td>Hardturm</td>
      <td>Zurich</td>
      <td>Hungary</td>
      <td>9</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>VINCENTI Raymond (FRA)</td>
      <td>VON GUNTER Albert (SUI)</td>
      <td>STEINER Carl (AUT)</td>
      <td>211</td>
      <td>1294</td>
      <td>HUN</td>
      <td>KOR</td>
      <td>9</td>
      <td>4</td>
    </tr>
    <tr>
      <th>88</th>
      <td>1954</td>
      <td>20 Jun 1954 - 17:00</td>
      <td>Group 2</td>
      <td>Charmilles</td>
      <td>Geneva</td>
      <td>Turkey</td>
      <td>7</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>MARINO Esteban (URU)</td>
      <td>ORLANDINI Vincenzo (ITA)</td>
      <td>SCHONHOLZER Ernest (SUI)</td>
      <td>211</td>
      <td>1304</td>
      <td>TUR</td>
      <td>KOR</td>
      <td>7</td>
      <td>4</td>
    </tr>
    <tr>
      <th>171</th>
      <td>1966</td>
      <td>12 Jul 1966 - 19:30</td>
      <td>Group 4</td>
      <td>Ayresome Park</td>
      <td>Middlesbrough</td>
      <td>Soviet Union</td>
      <td>3</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>GARDEAZABAL Juan (ESP)</td>
      <td>KANDIL Aly Hussein (EGY)</td>
      <td>DIENST Gottfried (SUI)</td>
      <td>238</td>
      <td>1710</td>
      <td>URS</td>
      <td>NSK</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>195</th>
      <td>1966</td>
      <td>23 Jul 1966 - 15:00</td>
      <td>Quarter-finals</td>
      <td>Goodison Park</td>
      <td>Liverpool</td>
      <td>Portugal</td>
      <td>5</td>
      <td>3</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>3</td>
      <td>ASHKENAZI Menachem (ISR)</td>
      <td>GALBA Karol (TCH)</td>
      <td>SCHWINTE Pierre (FRA)</td>
      <td>239</td>
      <td>1702</td>
      <td>POR</td>
      <td>NSK</td>
      <td>8</td>
      <td>5</td>
    </tr>
    <tr>
      <th>364</th>
      <td>1986</td>
      <td>02 Jun 1986 - 12:00</td>
      <td>Group A</td>
      <td>Estadio Ol�mpico Universitario</td>
      <td>Mexico City</td>
      <td>Argentina</td>
      <td>3</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>SANCHEZ ARMINIO Victoriano (ESP)</td>
      <td>GONZALEZ ROA Gabriel (PAR)</td>
      <td>DIAZ PALACIO Jesus (COL)</td>
      <td>308</td>
      <td>395</td>
      <td>ARG</td>
      <td>KOR</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>421</th>
      <td>1990</td>
      <td>12 Jun 1990 - 17:00</td>
      <td>Group E</td>
      <td>Marc Antonio Bentegodi</td>
      <td>Verona</td>
      <td>Belgium</td>
      <td>2</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>MAURO Vincent (USA)</td>
      <td>SNODDY Alan (NIR)</td>
      <td>COURTNEY George (ENG)</td>
      <td>322</td>
      <td>57</td>
      <td>BEL</td>
      <td>KOR</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>464</th>
      <td>1994</td>
      <td>17 Jun 1994 - 19:30</td>
      <td>Group C</td>
      <td>Cotton Bowl</td>
      <td>Dallas</td>
      <td>Spain</td>
      <td>2</td>
      <td>2</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>MIKKELSEN Peter (DEN)</td>
      <td>CHRISTENSEN Carl-Johan Meyer (DEN)</td>
      <td>PEARSON Roy (ENG)</td>
      <td>337</td>
      <td>3050</td>
      <td>ESP</td>
      <td>KOR</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>490</th>
      <td>1994</td>
      <td>27 Jun 1994 - 16:00</td>
      <td>Group C</td>
      <td>Cotton Bowl</td>
      <td>Dallas</td>
      <td>Germany</td>
      <td>3</td>
      <td>2</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>QUINIOU Joel (FRA)</td>
      <td>IVANOV Valentin (RUS)</td>
      <td>HASSAN Abdel-Magid (EGY)</td>
      <td>337</td>
      <td>3076</td>
      <td>GER</td>
      <td>KOR</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>542</th>
      <td>1998</td>
      <td>20 Jun 1998 - 21:00</td>
      <td>Group E</td>
      <td>Stade V�lodrome</td>
      <td>Marseilles</td>
      <td>Netherlands</td>
      <td>5</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>WOJCIK Ryszard (POL)</td>
      <td>POCIEGIEL Jacek (POL)</td>
      <td>DUPANOV Yuri (BLR)</td>
      <td>1014</td>
      <td>8749</td>
      <td>NED</td>
      <td>KOR</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>556</th>
      <td>1998</td>
      <td>25 Jun 1998 - 16:00</td>
      <td>Group E</td>
      <td>Parc des Princes</td>
      <td>Paris</td>
      <td>Belgium</td>
      <td>1</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>REZENDE Marcio (BRA)</td>
      <td>PINTO Arnaldo (BRA)</td>
      <td>ARANGO Jorge Luis (COL)</td>
      <td>1014</td>
      <td>8765</td>
      <td>BEL</td>
      <td>KOR</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>625</th>
      <td>2002</td>
      <td>14 Jun 2002 - 20:30</td>
      <td>Group D</td>
      <td>Incheon Football Stadium</td>
      <td>Incheon</td>
      <td>Portugal</td>
      <td>0</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>SANCHEZ Angel (ARG)</td>
      <td>ALTRAIFI Ali (KSA)</td>
      <td>SZEKELY Ferenc (HUN)</td>
      <td>43950100</td>
      <td>43950047</td>
      <td>POR</td>
      <td>KOR</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>639</th>
      <td>2002</td>
      <td>22 Jun 2002 - 15:30</td>
      <td>Quarter-finals</td>
      <td>Gwangju World Cup Stadium</td>
      <td>Gwangju</td>
      <td>Spain</td>
      <td>0</td>
      <td>0</td>
      <td>Korea</td>
      <td>Korea Republic win on penalties (3 - 5)</td>
      <td>...</td>
      <td>0</td>
      <td>EL GHANDOUR Gamal (EGY)</td>
      <td>TOMUSANGE Ali (UGA)</td>
      <td>RAGOONATH Michael (TRI)</td>
      <td>43950300</td>
      <td>43950059</td>
      <td>ESP</td>
      <td>KOR</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>640</th>
      <td>2002</td>
      <td>25 Jun 2002 - 20:30</td>
      <td>Semi-finals</td>
      <td>Seoul World Cup Stadium</td>
      <td>Seoul</td>
      <td>Germany</td>
      <td>1</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>MEIER Urs (SUI)</td>
      <td>ARNAULT Frederic (FRA)</td>
      <td>AMLER Evzen (CZE)</td>
      <td>43950400</td>
      <td>43950061</td>
      <td>GER</td>
      <td>KOR</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>672</th>
      <td>2006</td>
      <td>18 Jun 2006 - 21:00</td>
      <td>Group G</td>
      <td>Zentralstadion</td>
      <td>Leipzig</td>
      <td>France</td>
      <td>1</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>ARCHUNDIA Benito (MEX)</td>
      <td>RAMIREZ Jose (MEX)</td>
      <td>VERGARA Hector (CAN)</td>
      <td>97410100</td>
      <td>97410029</td>
      <td>FRA</td>
      <td>KOR</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>691</th>
      <td>2006</td>
      <td>23 Jun 2006 - 21:00</td>
      <td>Group G</td>
      <td>FIFA World Cup Stadium, Hanover</td>
      <td>Hanover</td>
      <td>Switzerland</td>
      <td>2</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>ELIZONDO Horacio (ARG)</td>
      <td>GARCIA Dario (ARG)</td>
      <td>OTERO Rodolfo (ARG)</td>
      <td>97410100</td>
      <td>97410046</td>
      <td>SUI</td>
      <td>KOR</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>721</th>
      <td>2010</td>
      <td>15 Jun 2010 - 20:30</td>
      <td>Group G</td>
      <td>Ellis Park Stadium</td>
      <td>Johannesburg</td>
      <td>Brazil</td>
      <td>2</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>KASSAI Viktor (HUN)</td>
      <td>EROS Gabor (HUN)</td>
      <td>VAMOS Tibor (HUN)</td>
      <td>249722</td>
      <td>300061490</td>
      <td>BRA</td>
      <td>NSK</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>725</th>
      <td>2010</td>
      <td>17 Jun 2010 - 13:30</td>
      <td>Group B</td>
      <td>Soccer City Stadium</td>
      <td>Johannesburg</td>
      <td>Argentina</td>
      <td>4</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>DE BLEECKERE Frank (BEL)</td>
      <td>HERMANS Peter (BEL)</td>
      <td>VROMANS Walter (BEL)</td>
      <td>249722</td>
      <td>300061458</td>
      <td>ARG</td>
      <td>KOR</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>737</th>
      <td>2010</td>
      <td>21 Jun 2010 - 13:30</td>
      <td>Group G</td>
      <td>Cape Town Stadium</td>
      <td>Cape Town</td>
      <td>Portugal</td>
      <td>7</td>
      <td>0</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>POZO Pablo (CHI)</td>
      <td>BASUALTO Patricio (CHI)</td>
      <td>MONDRIA Francisco (CHI)</td>
      <td>249722</td>
      <td>300061487</td>
      <td>POR</td>
      <td>NSK</td>
      <td>7</td>
      <td>1</td>
    </tr>
    <tr>
      <th>742</th>
      <td>2010</td>
      <td>22 Jun 2010 - 20:30</td>
      <td>Group B</td>
      <td>Durban Stadium</td>
      <td>Durban</td>
      <td>Nigeria</td>
      <td>2</td>
      <td>2</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>1</td>
      <td>Oleg�rio BENQUEREN�A (POR)</td>
      <td>CARDINAL Jose (POR)</td>
      <td>MIRANDA Bertino (POR)</td>
      <td>249722</td>
      <td>300111115</td>
      <td>NGA</td>
      <td>KOR</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>756</th>
      <td>2010</td>
      <td>26 Jun 2010 - 16:00</td>
      <td>Round of 16</td>
      <td>Port Elizabeth Stadium</td>
      <td>Nelson Mandela Bay/Port Elizabeth</td>
      <td>Uruguay</td>
      <td>2</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>Wolfgang STARK (GER)</td>
      <td>SALVER Jan-Hendrik (GER)</td>
      <td>PICKEL Mike (GER)</td>
      <td>249717</td>
      <td>300061504</td>
      <td>URU</td>
      <td>KOR</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>788</th>
      <td>2014</td>
      <td>17 Jun 2014 - 18:00</td>
      <td>Group H</td>
      <td>Arena Pantanal</td>
      <td>Cuiaba</td>
      <td>Russia</td>
      <td>1</td>
      <td>1</td>
      <td>Korea</td>
      <td></td>
      <td>...</td>
      <td>0</td>
      <td>PITANA Nestor (ARG)</td>
      <td>MAIDANA Hernan (ARG)</td>
      <td>BELATTI Juan Pablo (ARG)</td>
      <td>255931</td>
      <td>300186499</td>
      <td>RUS</td>
      <td>KOR</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>21 rows × 22 columns</p>
</div>


