
# Class Activity 1 정답


```python
import pandas as pd;
import numpy as np;
```

## 1


```python
s1 = pd.Series([10, 20, np.nan])
s1.index = ['a', 'b', 'c']
s1
```




    a    10.0
    b    20.0
    c     NaN
    dtype: float64



## 2


```python
s2 = pd.Series({'a':100, 'ㄴ':200, 'c':300})
s2
```




    a    100
    ㄴ    200
    c    300
    dtype: int64



## 3


```python
s2 = pd.Series(data = [1,2,3,4], index = ['한국','Japan','USA','중국'])
s2
```




    한국       1
    Japan    2
    USA      3
    중국       4
    dtype: int64



## 4


```python
S1 = pd.Series({'제주':10, '부산':20, '강원':30, '수원':25})
S2 = pd.Series({'강원':5, '부산':5, '제주':6})
S1+S2
```




    강원    35.0
    부산    25.0
    수원     NaN
    제주    16.0
    dtype: float64



## 5


```python
pwd
```




    'C:\\Users\\YechanEmbedded'



## 6


```python
df = pd.read_csv('JupyterData/gapminder.csv')
df.drop(labels = 'Unnamed: 0', axis = 1, inplace = True) # labels = 생략 가능 , inplace = True 생략 시 df에 적용안됨.
df
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>asia</td>
      <td>Philippines</td>
      <td>6598.0</td>
      <td>70.70</td>
      <td>100102249.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>americas</td>
      <td>Paraguay</td>
      <td>8038.0</td>
      <td>74.30</td>
      <td>6552584.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014</td>
      <td>asia</td>
      <td>Palau</td>
      <td>14078.0</td>
      <td>NaN</td>
      <td>21094.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2014</td>
      <td>asia</td>
      <td>Pakistan</td>
      <td>4619.0</td>
      <td>65.60</td>
      <td>185546257.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6277.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2014</td>
      <td>americas</td>
      <td>Brazil</td>
      <td>15412.0</td>
      <td>74.30</td>
      <td>204213133.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2014</td>
      <td>africa</td>
      <td>Nigeria</td>
      <td>5607.0</td>
      <td>63.70</td>
      <td>176460502.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2014</td>
      <td>americas</td>
      <td>Nicaragua</td>
      <td>4574.0</td>
      <td>77.80</td>
      <td>6013997.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2014</td>
      <td>europe</td>
      <td>Netherlands</td>
      <td>45281.0</td>
      <td>81.30</td>
      <td>16889356.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2014</td>
      <td>asia</td>
      <td>Papua New Guinea</td>
      <td>2510.0</td>
      <td>60.50</td>
      <td>7755785.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2014</td>
      <td>asia</td>
      <td>Taiwan</td>
      <td>41376.0</td>
      <td>79.40</td>
      <td>23184000.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2014</td>
      <td>americas</td>
      <td>St. Vincent and the Grenadines</td>
      <td>10131.0</td>
      <td>71.10</td>
      <td>109357.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2014</td>
      <td>americas</td>
      <td>Colombia</td>
      <td>12447.0</td>
      <td>77.80</td>
      <td>47791911.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2014</td>
      <td>europe</td>
      <td>Austria</td>
      <td>43906.0</td>
      <td>81.20</td>
      <td>8633220.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2014</td>
      <td>asia</td>
      <td>New Zealand</td>
      <td>33538.0</td>
      <td>81.40</td>
      <td>4566700.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2014</td>
      <td>americas</td>
      <td>Mexico</td>
      <td>16496.0</td>
      <td>75.60</td>
      <td>124221600.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mauritania</td>
      <td>3718.0</td>
      <td>69.60</td>
      <td>4063920.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2014</td>
      <td>africa</td>
      <td>Congo, Dem. Rep.</td>
      <td>768.0</td>
      <td>60.10</td>
      <td>73722860.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2014</td>
      <td>europe</td>
      <td>Malta</td>
      <td>29508.0</td>
      <td>82.00</td>
      <td>425570.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mali</td>
      <td>1653.0</td>
      <td>60.00</td>
      <td>16962846.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2014</td>
      <td>europe</td>
      <td>Armenia</td>
      <td>7763.0</td>
      <td>74.50</td>
      <td>2906220.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2014</td>
      <td>asia</td>
      <td>Malaysia</td>
      <td>23579.0</td>
      <td>75.10</td>
      <td>30228017.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2014</td>
      <td>africa</td>
      <td>Malawi</td>
      <td>778.0</td>
      <td>60.10</td>
      <td>17068838.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2014</td>
      <td>asia</td>
      <td>Oman</td>
      <td>48201.0</td>
      <td>77.00</td>
      <td>3960925.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2014</td>
      <td>asia</td>
      <td>Maldives</td>
      <td>14095.0</td>
      <td>80.00</td>
      <td>408247.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2014</td>
      <td>europe</td>
      <td>Macedonia, FYR</td>
      <td>12096.0</td>
      <td>76.20</td>
      <td>2077495.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2014</td>
      <td>africa</td>
      <td>Libya</td>
      <td>14887.0</td>
      <td>75.00</td>
      <td>6204108.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mozambique</td>
      <td>1115.0</td>
      <td>56.10</td>
      <td>27212382.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>54459</th>
      <td>1800</td>
      <td>americas</td>
      <td>Venezuela</td>
      <td>682.0</td>
      <td>32.20</td>
      <td>718000.0</td>
    </tr>
    <tr>
      <th>54460</th>
      <td>1800</td>
      <td>africa</td>
      <td>Zambia</td>
      <td>663.0</td>
      <td>32.60</td>
      <td>747000.0</td>
    </tr>
    <tr>
      <th>54461</th>
      <td>1800</td>
      <td>europe</td>
      <td>Croatia</td>
      <td>NaN</td>
      <td>36.10</td>
      <td>1227886.0</td>
    </tr>
    <tr>
      <th>54462</th>
      <td>1800</td>
      <td>europe</td>
      <td>Jersey</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>24420.0</td>
    </tr>
    <tr>
      <th>54463</th>
      <td>1800</td>
      <td>africa</td>
      <td>Reunion</td>
      <td>NaN</td>
      <td>33.00</td>
      <td>92744.0</td>
    </tr>
    <tr>
      <th>54464</th>
      <td>1800</td>
      <td>americas</td>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>33.40</td>
      <td>40000.0</td>
    </tr>
    <tr>
      <th>54465</th>
      <td>1800</td>
      <td>africa</td>
      <td>Western Sahara</td>
      <td>NaN</td>
      <td>34.75</td>
      <td>2788.0</td>
    </tr>
    <tr>
      <th>54466</th>
      <td>1800</td>
      <td>europe</td>
      <td>Akrotiri and Dhekelia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3710.0</td>
    </tr>
    <tr>
      <th>54467</th>
      <td>1800</td>
      <td>asia</td>
      <td>North Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782615.0</td>
    </tr>
    <tr>
      <th>54468</th>
      <td>1800</td>
      <td>europe</td>
      <td>Åland</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7135.0</td>
    </tr>
    <tr>
      <th>54469</th>
      <td>1800</td>
      <td>asia</td>
      <td>American Samoa</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8170.0</td>
    </tr>
    <tr>
      <th>54470</th>
      <td>1800</td>
      <td>europe</td>
      <td>Czechoslovakia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7007842.0</td>
    </tr>
    <tr>
      <th>54471</th>
      <td>1800</td>
      <td>europe</td>
      <td>USSR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>48539653.0</td>
    </tr>
    <tr>
      <th>54472</th>
      <td>1800</td>
      <td>americas</td>
      <td>Falkland Is (Malvinas)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>54473</th>
      <td>1800</td>
      <td>europe</td>
      <td>Gibraltar</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>9873.0</td>
    </tr>
    <tr>
      <th>54474</th>
      <td>1800</td>
      <td>europe</td>
      <td>Isle of Man</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>23533.0</td>
    </tr>
    <tr>
      <th>54475</th>
      <td>1800</td>
      <td>europe</td>
      <td>Liechtenstein</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5802.0</td>
    </tr>
    <tr>
      <th>54476</th>
      <td>1800</td>
      <td>americas</td>
      <td>Montserrat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5230.0</td>
    </tr>
    <tr>
      <th>54477</th>
      <td>1800</td>
      <td>asia</td>
      <td>Norfolk Island</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1121.0</td>
    </tr>
    <tr>
      <th>54478</th>
      <td>1800</td>
      <td>asia</td>
      <td>Northern Mariana Islands</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3360.0</td>
    </tr>
    <tr>
      <th>54479</th>
      <td>1800</td>
      <td>europe</td>
      <td>Serbia and Montenegro</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2273780.0</td>
    </tr>
    <tr>
      <th>54480</th>
      <td>1800</td>
      <td>asia</td>
      <td>South Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>551928.0</td>
    </tr>
    <tr>
      <th>54481</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Barthélemy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2515.0</td>
    </tr>
    <tr>
      <th>54482</th>
      <td>1800</td>
      <td>africa</td>
      <td>St. Helena</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1997.0</td>
    </tr>
    <tr>
      <th>54483</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Martin</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5380.0</td>
    </tr>
    <tr>
      <th>54484</th>
      <td>1800</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782.0</td>
    </tr>
    <tr>
      <th>54485</th>
      <td>1800</td>
      <td>europe</td>
      <td>Svalbard</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>54486</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tokelau</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1009.0</td>
    </tr>
    <tr>
      <th>54487</th>
      <td>1800</td>
      <td>asia</td>
      <td>United Korea (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13740000.0</td>
    </tr>
    <tr>
      <th>54488</th>
      <td>1800</td>
      <td>europe</td>
      <td>Yugoslavia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4687422.0</td>
    </tr>
  </tbody>
</table>
<p>54489 rows × 6 columns</p>
</div>



## 7


```python
df.head(5) # default = 5이므로 인자 생략 가능
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>asia</td>
      <td>Philippines</td>
      <td>6598.0</td>
      <td>70.7</td>
      <td>100102249.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>americas</td>
      <td>Paraguay</td>
      <td>8038.0</td>
      <td>74.3</td>
      <td>6552584.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014</td>
      <td>asia</td>
      <td>Palau</td>
      <td>14078.0</td>
      <td>NaN</td>
      <td>21094.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2014</td>
      <td>asia</td>
      <td>Pakistan</td>
      <td>4619.0</td>
      <td>65.6</td>
      <td>185546257.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6277.0</td>
    </tr>
  </tbody>
</table>
</div>



## 8


```python
df.tail(5) # default = 5이므로 인자 생략 가능
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>54484</th>
      <td>1800</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782.0</td>
    </tr>
    <tr>
      <th>54485</th>
      <td>1800</td>
      <td>europe</td>
      <td>Svalbard</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>54486</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tokelau</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1009.0</td>
    </tr>
    <tr>
      <th>54487</th>
      <td>1800</td>
      <td>asia</td>
      <td>United Korea (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13740000.0</td>
    </tr>
    <tr>
      <th>54488</th>
      <td>1800</td>
      <td>europe</td>
      <td>Yugoslavia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4687422.0</td>
    </tr>
  </tbody>
</table>
</div>



## 9


```python
df['income']
```




    0          6598.0
    1          8038.0
    2         14078.0
    3          4619.0
    4             NaN
    5         15412.0
    6         64020.0
    7          5607.0
    8          4574.0
    9         45281.0
    10         2510.0
    11        41376.0
    12        10131.0
    13        12447.0
    14        43906.0
    15        33538.0
    16        16496.0
    17         3718.0
    18          768.0
    19        29508.0
    20         1653.0
    21         7763.0
    22        23579.0
    23          778.0
    24        48201.0
    25        14095.0
    26        12096.0
    27       142893.0
    28        14887.0
    29         1115.0
               ...   
    54459       682.0
    54460       663.0
    54461         NaN
    54462         NaN
    54463         NaN
    54464         NaN
    54465         NaN
    54466         NaN
    54467         NaN
    54468         NaN
    54469         NaN
    54470         NaN
    54471         NaN
    54472         NaN
    54473         NaN
    54474         NaN
    54475         NaN
    54476         NaN
    54477         NaN
    54478         NaN
    54479         NaN
    54480         NaN
    54481         NaN
    54482         NaN
    54483         NaN
    54484         NaN
    54485         NaN
    54486         NaN
    54487         NaN
    54488         NaN
    Name: income, Length: 54489, dtype: float64



## 10


```python
df['income'][3:5]
```




    3    4619.0
    4       NaN
    Name: income, dtype: float64



## 11


```python
df['gross_income'] = df['population'] * df['income']
df
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>asia</td>
      <td>Philippines</td>
      <td>6598.0</td>
      <td>70.70</td>
      <td>100102249.0</td>
      <td>6.604746e+11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>americas</td>
      <td>Paraguay</td>
      <td>8038.0</td>
      <td>74.30</td>
      <td>6552584.0</td>
      <td>5.266967e+10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014</td>
      <td>asia</td>
      <td>Palau</td>
      <td>14078.0</td>
      <td>NaN</td>
      <td>21094.0</td>
      <td>2.969613e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2014</td>
      <td>asia</td>
      <td>Pakistan</td>
      <td>4619.0</td>
      <td>65.60</td>
      <td>185546257.0</td>
      <td>8.570382e+11</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6277.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2014</td>
      <td>americas</td>
      <td>Brazil</td>
      <td>15412.0</td>
      <td>74.30</td>
      <td>204213133.0</td>
      <td>3.147333e+12</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
      <td>3.290827e+11</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2014</td>
      <td>africa</td>
      <td>Nigeria</td>
      <td>5607.0</td>
      <td>63.70</td>
      <td>176460502.0</td>
      <td>9.894140e+11</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2014</td>
      <td>americas</td>
      <td>Nicaragua</td>
      <td>4574.0</td>
      <td>77.80</td>
      <td>6013997.0</td>
      <td>2.750802e+10</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2014</td>
      <td>europe</td>
      <td>Netherlands</td>
      <td>45281.0</td>
      <td>81.30</td>
      <td>16889356.0</td>
      <td>7.647669e+11</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2014</td>
      <td>asia</td>
      <td>Papua New Guinea</td>
      <td>2510.0</td>
      <td>60.50</td>
      <td>7755785.0</td>
      <td>1.946702e+10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2014</td>
      <td>asia</td>
      <td>Taiwan</td>
      <td>41376.0</td>
      <td>79.40</td>
      <td>23184000.0</td>
      <td>9.592612e+11</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2014</td>
      <td>americas</td>
      <td>St. Vincent and the Grenadines</td>
      <td>10131.0</td>
      <td>71.10</td>
      <td>109357.0</td>
      <td>1.107896e+09</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2014</td>
      <td>americas</td>
      <td>Colombia</td>
      <td>12447.0</td>
      <td>77.80</td>
      <td>47791911.0</td>
      <td>5.948659e+11</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2014</td>
      <td>europe</td>
      <td>Austria</td>
      <td>43906.0</td>
      <td>81.20</td>
      <td>8633220.0</td>
      <td>3.790502e+11</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2014</td>
      <td>asia</td>
      <td>New Zealand</td>
      <td>33538.0</td>
      <td>81.40</td>
      <td>4566700.0</td>
      <td>1.531580e+11</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2014</td>
      <td>americas</td>
      <td>Mexico</td>
      <td>16496.0</td>
      <td>75.60</td>
      <td>124221600.0</td>
      <td>2.049160e+12</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mauritania</td>
      <td>3718.0</td>
      <td>69.60</td>
      <td>4063920.0</td>
      <td>1.510965e+10</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2014</td>
      <td>africa</td>
      <td>Congo, Dem. Rep.</td>
      <td>768.0</td>
      <td>60.10</td>
      <td>73722860.0</td>
      <td>5.661916e+10</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2014</td>
      <td>europe</td>
      <td>Malta</td>
      <td>29508.0</td>
      <td>82.00</td>
      <td>425570.0</td>
      <td>1.255772e+10</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mali</td>
      <td>1653.0</td>
      <td>60.00</td>
      <td>16962846.0</td>
      <td>2.803958e+10</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2014</td>
      <td>europe</td>
      <td>Armenia</td>
      <td>7763.0</td>
      <td>74.50</td>
      <td>2906220.0</td>
      <td>2.256099e+10</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2014</td>
      <td>asia</td>
      <td>Malaysia</td>
      <td>23579.0</td>
      <td>75.10</td>
      <td>30228017.0</td>
      <td>7.127464e+11</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2014</td>
      <td>africa</td>
      <td>Malawi</td>
      <td>778.0</td>
      <td>60.10</td>
      <td>17068838.0</td>
      <td>1.327956e+10</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2014</td>
      <td>asia</td>
      <td>Oman</td>
      <td>48201.0</td>
      <td>77.00</td>
      <td>3960925.0</td>
      <td>1.909205e+11</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2014</td>
      <td>asia</td>
      <td>Maldives</td>
      <td>14095.0</td>
      <td>80.00</td>
      <td>408247.0</td>
      <td>5.754241e+09</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2014</td>
      <td>europe</td>
      <td>Macedonia, FYR</td>
      <td>12096.0</td>
      <td>76.20</td>
      <td>2077495.0</td>
      <td>2.512938e+10</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2014</td>
      <td>africa</td>
      <td>Libya</td>
      <td>14887.0</td>
      <td>75.00</td>
      <td>6204108.0</td>
      <td>9.236056e+10</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mozambique</td>
      <td>1115.0</td>
      <td>56.10</td>
      <td>27212382.0</td>
      <td>3.034181e+10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>54459</th>
      <td>1800</td>
      <td>americas</td>
      <td>Venezuela</td>
      <td>682.0</td>
      <td>32.20</td>
      <td>718000.0</td>
      <td>4.896760e+08</td>
    </tr>
    <tr>
      <th>54460</th>
      <td>1800</td>
      <td>africa</td>
      <td>Zambia</td>
      <td>663.0</td>
      <td>32.60</td>
      <td>747000.0</td>
      <td>4.952610e+08</td>
    </tr>
    <tr>
      <th>54461</th>
      <td>1800</td>
      <td>europe</td>
      <td>Croatia</td>
      <td>NaN</td>
      <td>36.10</td>
      <td>1227886.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54462</th>
      <td>1800</td>
      <td>europe</td>
      <td>Jersey</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>24420.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54463</th>
      <td>1800</td>
      <td>africa</td>
      <td>Reunion</td>
      <td>NaN</td>
      <td>33.00</td>
      <td>92744.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54464</th>
      <td>1800</td>
      <td>americas</td>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>33.40</td>
      <td>40000.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54465</th>
      <td>1800</td>
      <td>africa</td>
      <td>Western Sahara</td>
      <td>NaN</td>
      <td>34.75</td>
      <td>2788.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54466</th>
      <td>1800</td>
      <td>europe</td>
      <td>Akrotiri and Dhekelia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3710.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54467</th>
      <td>1800</td>
      <td>asia</td>
      <td>North Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782615.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54468</th>
      <td>1800</td>
      <td>europe</td>
      <td>Åland</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7135.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54469</th>
      <td>1800</td>
      <td>asia</td>
      <td>American Samoa</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8170.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54470</th>
      <td>1800</td>
      <td>europe</td>
      <td>Czechoslovakia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7007842.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54471</th>
      <td>1800</td>
      <td>europe</td>
      <td>USSR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>48539653.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54472</th>
      <td>1800</td>
      <td>americas</td>
      <td>Falkland Is (Malvinas)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54473</th>
      <td>1800</td>
      <td>europe</td>
      <td>Gibraltar</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>9873.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54474</th>
      <td>1800</td>
      <td>europe</td>
      <td>Isle of Man</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>23533.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54475</th>
      <td>1800</td>
      <td>europe</td>
      <td>Liechtenstein</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5802.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54476</th>
      <td>1800</td>
      <td>americas</td>
      <td>Montserrat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5230.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54477</th>
      <td>1800</td>
      <td>asia</td>
      <td>Norfolk Island</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1121.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54478</th>
      <td>1800</td>
      <td>asia</td>
      <td>Northern Mariana Islands</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3360.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54479</th>
      <td>1800</td>
      <td>europe</td>
      <td>Serbia and Montenegro</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2273780.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54480</th>
      <td>1800</td>
      <td>asia</td>
      <td>South Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>551928.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54481</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Barthélemy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2515.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54482</th>
      <td>1800</td>
      <td>africa</td>
      <td>St. Helena</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1997.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54483</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Martin</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5380.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54484</th>
      <td>1800</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54485</th>
      <td>1800</td>
      <td>europe</td>
      <td>Svalbard</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54486</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tokelau</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1009.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54487</th>
      <td>1800</td>
      <td>asia</td>
      <td>United Korea (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13740000.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54488</th>
      <td>1800</td>
      <td>europe</td>
      <td>Yugoslavia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4687422.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>54489 rows × 7 columns</p>
</div>



## 12


```python
df.drop(index = 5, axis = 1)
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>asia</td>
      <td>Philippines</td>
      <td>6598.0</td>
      <td>70.70</td>
      <td>100102249.0</td>
      <td>6.604746e+11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>americas</td>
      <td>Paraguay</td>
      <td>8038.0</td>
      <td>74.30</td>
      <td>6552584.0</td>
      <td>5.266967e+10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014</td>
      <td>asia</td>
      <td>Palau</td>
      <td>14078.0</td>
      <td>NaN</td>
      <td>21094.0</td>
      <td>2.969613e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2014</td>
      <td>asia</td>
      <td>Pakistan</td>
      <td>4619.0</td>
      <td>65.60</td>
      <td>185546257.0</td>
      <td>8.570382e+11</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6277.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
      <td>3.290827e+11</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2014</td>
      <td>africa</td>
      <td>Nigeria</td>
      <td>5607.0</td>
      <td>63.70</td>
      <td>176460502.0</td>
      <td>9.894140e+11</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2014</td>
      <td>americas</td>
      <td>Nicaragua</td>
      <td>4574.0</td>
      <td>77.80</td>
      <td>6013997.0</td>
      <td>2.750802e+10</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2014</td>
      <td>europe</td>
      <td>Netherlands</td>
      <td>45281.0</td>
      <td>81.30</td>
      <td>16889356.0</td>
      <td>7.647669e+11</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2014</td>
      <td>asia</td>
      <td>Papua New Guinea</td>
      <td>2510.0</td>
      <td>60.50</td>
      <td>7755785.0</td>
      <td>1.946702e+10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2014</td>
      <td>asia</td>
      <td>Taiwan</td>
      <td>41376.0</td>
      <td>79.40</td>
      <td>23184000.0</td>
      <td>9.592612e+11</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2014</td>
      <td>americas</td>
      <td>St. Vincent and the Grenadines</td>
      <td>10131.0</td>
      <td>71.10</td>
      <td>109357.0</td>
      <td>1.107896e+09</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2014</td>
      <td>americas</td>
      <td>Colombia</td>
      <td>12447.0</td>
      <td>77.80</td>
      <td>47791911.0</td>
      <td>5.948659e+11</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2014</td>
      <td>europe</td>
      <td>Austria</td>
      <td>43906.0</td>
      <td>81.20</td>
      <td>8633220.0</td>
      <td>3.790502e+11</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2014</td>
      <td>asia</td>
      <td>New Zealand</td>
      <td>33538.0</td>
      <td>81.40</td>
      <td>4566700.0</td>
      <td>1.531580e+11</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2014</td>
      <td>americas</td>
      <td>Mexico</td>
      <td>16496.0</td>
      <td>75.60</td>
      <td>124221600.0</td>
      <td>2.049160e+12</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mauritania</td>
      <td>3718.0</td>
      <td>69.60</td>
      <td>4063920.0</td>
      <td>1.510965e+10</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2014</td>
      <td>africa</td>
      <td>Congo, Dem. Rep.</td>
      <td>768.0</td>
      <td>60.10</td>
      <td>73722860.0</td>
      <td>5.661916e+10</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2014</td>
      <td>europe</td>
      <td>Malta</td>
      <td>29508.0</td>
      <td>82.00</td>
      <td>425570.0</td>
      <td>1.255772e+10</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mali</td>
      <td>1653.0</td>
      <td>60.00</td>
      <td>16962846.0</td>
      <td>2.803958e+10</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2014</td>
      <td>europe</td>
      <td>Armenia</td>
      <td>7763.0</td>
      <td>74.50</td>
      <td>2906220.0</td>
      <td>2.256099e+10</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2014</td>
      <td>asia</td>
      <td>Malaysia</td>
      <td>23579.0</td>
      <td>75.10</td>
      <td>30228017.0</td>
      <td>7.127464e+11</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2014</td>
      <td>africa</td>
      <td>Malawi</td>
      <td>778.0</td>
      <td>60.10</td>
      <td>17068838.0</td>
      <td>1.327956e+10</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2014</td>
      <td>asia</td>
      <td>Oman</td>
      <td>48201.0</td>
      <td>77.00</td>
      <td>3960925.0</td>
      <td>1.909205e+11</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2014</td>
      <td>asia</td>
      <td>Maldives</td>
      <td>14095.0</td>
      <td>80.00</td>
      <td>408247.0</td>
      <td>5.754241e+09</td>
    </tr>
    <tr>
      <th>26</th>
      <td>2014</td>
      <td>europe</td>
      <td>Macedonia, FYR</td>
      <td>12096.0</td>
      <td>76.20</td>
      <td>2077495.0</td>
      <td>2.512938e+10</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2014</td>
      <td>africa</td>
      <td>Libya</td>
      <td>14887.0</td>
      <td>75.00</td>
      <td>6204108.0</td>
      <td>9.236056e+10</td>
    </tr>
    <tr>
      <th>29</th>
      <td>2014</td>
      <td>africa</td>
      <td>Mozambique</td>
      <td>1115.0</td>
      <td>56.10</td>
      <td>27212382.0</td>
      <td>3.034181e+10</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2014</td>
      <td>americas</td>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>80.38</td>
      <td>105110.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>54459</th>
      <td>1800</td>
      <td>americas</td>
      <td>Venezuela</td>
      <td>682.0</td>
      <td>32.20</td>
      <td>718000.0</td>
      <td>4.896760e+08</td>
    </tr>
    <tr>
      <th>54460</th>
      <td>1800</td>
      <td>africa</td>
      <td>Zambia</td>
      <td>663.0</td>
      <td>32.60</td>
      <td>747000.0</td>
      <td>4.952610e+08</td>
    </tr>
    <tr>
      <th>54461</th>
      <td>1800</td>
      <td>europe</td>
      <td>Croatia</td>
      <td>NaN</td>
      <td>36.10</td>
      <td>1227886.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54462</th>
      <td>1800</td>
      <td>europe</td>
      <td>Jersey</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>24420.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54463</th>
      <td>1800</td>
      <td>africa</td>
      <td>Reunion</td>
      <td>NaN</td>
      <td>33.00</td>
      <td>92744.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54464</th>
      <td>1800</td>
      <td>americas</td>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>33.40</td>
      <td>40000.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54465</th>
      <td>1800</td>
      <td>africa</td>
      <td>Western Sahara</td>
      <td>NaN</td>
      <td>34.75</td>
      <td>2788.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54466</th>
      <td>1800</td>
      <td>europe</td>
      <td>Akrotiri and Dhekelia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3710.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54467</th>
      <td>1800</td>
      <td>asia</td>
      <td>North Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782615.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54468</th>
      <td>1800</td>
      <td>europe</td>
      <td>Åland</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7135.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54469</th>
      <td>1800</td>
      <td>asia</td>
      <td>American Samoa</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8170.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54470</th>
      <td>1800</td>
      <td>europe</td>
      <td>Czechoslovakia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7007842.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54471</th>
      <td>1800</td>
      <td>europe</td>
      <td>USSR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>48539653.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54472</th>
      <td>1800</td>
      <td>americas</td>
      <td>Falkland Is (Malvinas)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54473</th>
      <td>1800</td>
      <td>europe</td>
      <td>Gibraltar</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>9873.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54474</th>
      <td>1800</td>
      <td>europe</td>
      <td>Isle of Man</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>23533.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54475</th>
      <td>1800</td>
      <td>europe</td>
      <td>Liechtenstein</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5802.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54476</th>
      <td>1800</td>
      <td>americas</td>
      <td>Montserrat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5230.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54477</th>
      <td>1800</td>
      <td>asia</td>
      <td>Norfolk Island</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1121.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54478</th>
      <td>1800</td>
      <td>asia</td>
      <td>Northern Mariana Islands</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3360.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54479</th>
      <td>1800</td>
      <td>europe</td>
      <td>Serbia and Montenegro</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2273780.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54480</th>
      <td>1800</td>
      <td>asia</td>
      <td>South Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>551928.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54481</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Barthélemy</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2515.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54482</th>
      <td>1800</td>
      <td>africa</td>
      <td>St. Helena</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1997.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54483</th>
      <td>1800</td>
      <td>americas</td>
      <td>St. Martin</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5380.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54484</th>
      <td>1800</td>
      <td>americas</td>
      <td>St.-Pierre-et-Miquelon</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1782.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54485</th>
      <td>1800</td>
      <td>europe</td>
      <td>Svalbard</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54486</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tokelau</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1009.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54487</th>
      <td>1800</td>
      <td>asia</td>
      <td>United Korea (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13740000.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54488</th>
      <td>1800</td>
      <td>europe</td>
      <td>Yugoslavia</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4687422.0</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>54488 rows × 7 columns</p>
</div>



## 13


```python
df.loc[3]
```




    year                   2014
    continent              asia
    country            Pakistan
    income                 4619
    life_exp               65.6
    population      1.85546e+08
    gross_income    8.57038e+11
    Name: 3, dtype: object



## 14


```python
df.loc[3, 'country']
```




    'Pakistan'




```python
df.loc[3].country
```




    'Pakistan'



## 15


```python
df.loc[[10,100,1000], ['continent', 'country']]
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
      <th>continent</th>
      <th>country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10</th>
      <td>asia</td>
      <td>Papua New Guinea</td>
    </tr>
    <tr>
      <th>100</th>
      <td>africa</td>
      <td>Namibia</td>
    </tr>
    <tr>
      <th>1000</th>
      <td>africa</td>
      <td>Cape Verde</td>
    </tr>
  </tbody>
</table>
</div>



## 16


```python
df[df['income'] > 50000]
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
      <td>3.290827e+11</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2014</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>52552.0</td>
      <td>83.56</td>
      <td>7194563.0</td>
      <td>3.780887e+11</td>
    </tr>
    <tr>
      <th>56</th>
      <td>2014</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88203.0</td>
      <td>82.10</td>
      <td>556316.0</td>
      <td>4.906874e+10</td>
    </tr>
    <tr>
      <th>77</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kuwait</td>
      <td>83394.0</td>
      <td>80.20</td>
      <td>3782450.0</td>
      <td>3.154336e+11</td>
    </tr>
    <tr>
      <th>78</th>
      <td>2014</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>72219.0</td>
      <td>77.10</td>
      <td>411704.0</td>
      <td>2.973285e+10</td>
    </tr>
    <tr>
      <th>112</th>
      <td>2014</td>
      <td>asia</td>
      <td>United Arab Emirates</td>
      <td>60578.0</td>
      <td>75.40</td>
      <td>9070867.0</td>
      <td>5.494950e+11</td>
    </tr>
    <tr>
      <th>153</th>
      <td>2014</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>55776.0</td>
      <td>82.90</td>
      <td>8229629.0</td>
      <td>4.590158e+11</td>
    </tr>
    <tr>
      <th>157</th>
      <td>2014</td>
      <td>europe</td>
      <td>Monaco</td>
      <td>61738.0</td>
      <td>NaN</td>
      <td>38132.0</td>
      <td>2.354193e+09</td>
    </tr>
    <tr>
      <th>165</th>
      <td>2014</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>78958.0</td>
      <td>81.90</td>
      <td>5448342.0</td>
      <td>4.301902e+11</td>
    </tr>
    <tr>
      <th>173</th>
      <td>2014</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>133563.0</td>
      <td>79.80</td>
      <td>2374419.0</td>
      <td>3.171345e+11</td>
    </tr>
    <tr>
      <th>182</th>
      <td>2014</td>
      <td>asia</td>
      <td>Saudi Arabia</td>
      <td>52096.0</td>
      <td>79.40</td>
      <td>30776722.0</td>
      <td>1.603344e+12</td>
    </tr>
    <tr>
      <th>207</th>
      <td>2014</td>
      <td>americas</td>
      <td>United States</td>
      <td>52118.0</td>
      <td>79.10</td>
      <td>317718779.0</td>
      <td>1.655887e+13</td>
    </tr>
    <tr>
      <th>249</th>
      <td>2013</td>
      <td>europe</td>
      <td>Monaco</td>
      <td>57886.0</td>
      <td>NaN</td>
      <td>37971.0</td>
      <td>2.197989e+09</td>
    </tr>
    <tr>
      <th>252</th>
      <td>2013</td>
      <td>americas</td>
      <td>Bermuda</td>
      <td>50669.0</td>
      <td>78.30</td>
      <td>62771.0</td>
      <td>3.180544e+09</td>
    </tr>
    <tr>
      <th>264</th>
      <td>2013</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>136540.0</td>
      <td>80.40</td>
      <td>575841.0</td>
      <td>7.862533e+10</td>
    </tr>
    <tr>
      <th>265</th>
      <td>2013</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88850.0</td>
      <td>81.90</td>
      <td>544721.0</td>
      <td>4.839846e+10</td>
    </tr>
    <tr>
      <th>276</th>
      <td>2013</td>
      <td>asia</td>
      <td>Kuwait</td>
      <td>79395.0</td>
      <td>79.70</td>
      <td>3598385.0</td>
      <td>2.856938e+11</td>
    </tr>
    <tr>
      <th>280</th>
      <td>2013</td>
      <td>europe</td>
      <td>Norway</td>
      <td>63322.0</td>
      <td>81.60</td>
      <td>5077101.0</td>
      <td>3.214922e+11</td>
    </tr>
    <tr>
      <th>281</th>
      <td>2013</td>
      <td>asia</td>
      <td>Saudi Arabia</td>
      <td>51294.0</td>
      <td>79.30</td>
      <td>29944476.0</td>
      <td>1.535972e+12</td>
    </tr>
    <tr>
      <th>312</th>
      <td>2013</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>51656.0</td>
      <td>83.38</td>
      <td>7148571.0</td>
      <td>3.692666e+11</td>
    </tr>
    <tr>
      <th>372</th>
      <td>2013</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>69474.0</td>
      <td>76.90</td>
      <td>405716.0</td>
      <td>2.818671e+10</td>
    </tr>
    <tr>
      <th>416</th>
      <td>2013</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>131579.0</td>
      <td>79.90</td>
      <td>2250473.0</td>
      <td>2.961150e+11</td>
    </tr>
    <tr>
      <th>421</th>
      <td>2013</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>77721.0</td>
      <td>81.70</td>
      <td>5360837.0</td>
      <td>4.166496e+11</td>
    </tr>
    <tr>
      <th>435</th>
      <td>2013</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54983.0</td>
      <td>82.80</td>
      <td>8132674.0</td>
      <td>4.471588e+11</td>
    </tr>
    <tr>
      <th>437</th>
      <td>2013</td>
      <td>americas</td>
      <td>United States</td>
      <td>51282.0</td>
      <td>79.10</td>
      <td>315536676.0</td>
      <td>1.618135e+13</td>
    </tr>
    <tr>
      <th>442</th>
      <td>2013</td>
      <td>asia</td>
      <td>United Arab Emirates</td>
      <td>59092.0</td>
      <td>75.40</td>
      <td>9006263.0</td>
      <td>5.321981e+11</td>
    </tr>
    <tr>
      <th>484</th>
      <td>2012</td>
      <td>europe</td>
      <td>Monaco</td>
      <td>58081.0</td>
      <td>NaN</td>
      <td>37783.0</td>
      <td>2.194474e+09</td>
    </tr>
    <tr>
      <th>497</th>
      <td>2012</td>
      <td>americas</td>
      <td>Bermuda</td>
      <td>52137.0</td>
      <td>78.30</td>
      <td>63179.0</td>
      <td>3.293964e+09</td>
    </tr>
    <tr>
      <th>499</th>
      <td>2012</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>125515.0</td>
      <td>80.19</td>
      <td>562531.0</td>
      <td>7.060608e+10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>11188</th>
      <td>1970</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>158673.0</td>
      <td>67.91</td>
      <td>109514.0</td>
      <td>1.737691e+10</td>
    </tr>
    <tr>
      <th>11218</th>
      <td>1970</td>
      <td>africa</td>
      <td>Libya</td>
      <td>67491.0</td>
      <td>59.01</td>
      <td>2133526.0</td>
      <td>1.439938e+11</td>
    </tr>
    <tr>
      <th>11325</th>
      <td>1969</td>
      <td>asia</td>
      <td>Nauru</td>
      <td>50241.0</td>
      <td>NaN</td>
      <td>6371.0</td>
      <td>3.200854e+08</td>
    </tr>
    <tr>
      <th>11344</th>
      <td>1969</td>
      <td>africa</td>
      <td>Libya</td>
      <td>66299.0</td>
      <td>57.88</td>
      <td>2043818.0</td>
      <td>1.355031e+11</td>
    </tr>
    <tr>
      <th>11395</th>
      <td>1969</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>72988.0</td>
      <td>66.97</td>
      <td>123653.0</td>
      <td>9.025185e+09</td>
    </tr>
    <tr>
      <th>11491</th>
      <td>1969</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>125963.0</td>
      <td>67.29</td>
      <td>100874.0</td>
      <td>1.270639e+10</td>
    </tr>
    <tr>
      <th>11648</th>
      <td>1968</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>71861.0</td>
      <td>66.54</td>
      <td>117950.0</td>
      <td>8.476005e+09</td>
    </tr>
    <tr>
      <th>11685</th>
      <td>1968</td>
      <td>africa</td>
      <td>Libya</td>
      <td>60948.0</td>
      <td>56.69</td>
      <td>1958914.0</td>
      <td>1.193919e+11</td>
    </tr>
    <tr>
      <th>11755</th>
      <td>1968</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>99995.0</td>
      <td>66.64</td>
      <td>93201.0</td>
      <td>9.319634e+09</td>
    </tr>
    <tr>
      <th>11891</th>
      <td>1967</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>70751.0</td>
      <td>66.12</td>
      <td>112494.0</td>
      <td>7.959063e+09</td>
    </tr>
    <tr>
      <th>12000</th>
      <td>1967</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>79381.0</td>
      <td>65.95</td>
      <td>86295.0</td>
      <td>6.850183e+09</td>
    </tr>
    <tr>
      <th>12145</th>
      <td>1966</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>69658.0</td>
      <td>65.67</td>
      <td>107316.0</td>
      <td>7.475418e+09</td>
    </tr>
    <tr>
      <th>12216</th>
      <td>1966</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>63016.0</td>
      <td>65.25</td>
      <td>79844.0</td>
      <td>5.031450e+09</td>
    </tr>
    <tr>
      <th>12326</th>
      <td>1965</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>68582.0</td>
      <td>65.21</td>
      <td>102425.0</td>
      <td>7.024511e+09</td>
    </tr>
    <tr>
      <th>12465</th>
      <td>1965</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>50024.0</td>
      <td>64.53</td>
      <td>73633.0</td>
      <td>3.683417e+09</td>
    </tr>
    <tr>
      <th>12580</th>
      <td>1964</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>67522.0</td>
      <td>64.72</td>
      <td>97848.0</td>
      <td>6.606893e+09</td>
    </tr>
    <tr>
      <th>12913</th>
      <td>1963</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>66479.0</td>
      <td>64.21</td>
      <td>93576.0</td>
      <td>6.220839e+09</td>
    </tr>
    <tr>
      <th>13089</th>
      <td>1962</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>65451.0</td>
      <td>63.67</td>
      <td>89516.0</td>
      <td>5.858912e+09</td>
    </tr>
    <tr>
      <th>13344</th>
      <td>1961</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>64439.0</td>
      <td>63.11</td>
      <td>85596.0</td>
      <td>5.515721e+09</td>
    </tr>
    <tr>
      <th>13596</th>
      <td>1960</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>63442.0</td>
      <td>62.52</td>
      <td>81745.0</td>
      <td>5.186066e+09</td>
    </tr>
    <tr>
      <th>13932</th>
      <td>1959</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>62460.0</td>
      <td>61.93</td>
      <td>77919.0</td>
      <td>4.866821e+09</td>
    </tr>
    <tr>
      <th>14183</th>
      <td>1958</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>61493.0</td>
      <td>61.31</td>
      <td>74150.0</td>
      <td>4.559706e+09</td>
    </tr>
    <tr>
      <th>14444</th>
      <td>1957</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>60541.0</td>
      <td>60.70</td>
      <td>70457.0</td>
      <td>4.265537e+09</td>
    </tr>
    <tr>
      <th>14698</th>
      <td>1956</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>59604.0</td>
      <td>60.07</td>
      <td>66862.0</td>
      <td>3.985243e+09</td>
    </tr>
    <tr>
      <th>14935</th>
      <td>1955</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>58680.0</td>
      <td>59.45</td>
      <td>63420.0</td>
      <td>3.721486e+09</td>
    </tr>
    <tr>
      <th>15196</th>
      <td>1954</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>57771.0</td>
      <td>58.83</td>
      <td>60120.0</td>
      <td>3.473193e+09</td>
    </tr>
    <tr>
      <th>15455</th>
      <td>1953</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>56876.0</td>
      <td>58.22</td>
      <td>56968.0</td>
      <td>3.240112e+09</td>
    </tr>
    <tr>
      <th>15629</th>
      <td>1952</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>55994.0</td>
      <td>57.60</td>
      <td>53927.0</td>
      <td>3.019588e+09</td>
    </tr>
    <tr>
      <th>15951</th>
      <td>1951</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>55126.0</td>
      <td>56.99</td>
      <td>50961.0</td>
      <td>2.809276e+09</td>
    </tr>
    <tr>
      <th>16136</th>
      <td>1950</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>54271.0</td>
      <td>56.68</td>
      <td>48001.0</td>
      <td>2.605062e+09</td>
    </tr>
  </tbody>
</table>
<p>388 rows × 7 columns</p>
</div>



## 17


```python
df[(df['income'] > 50000) & (df['life_exp'] > 80)]
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
      <td>3.290827e+11</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2014</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>52552.0</td>
      <td>83.56</td>
      <td>7194563.0</td>
      <td>3.780887e+11</td>
    </tr>
    <tr>
      <th>56</th>
      <td>2014</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88203.0</td>
      <td>82.10</td>
      <td>556316.0</td>
      <td>4.906874e+10</td>
    </tr>
    <tr>
      <th>77</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kuwait</td>
      <td>83394.0</td>
      <td>80.20</td>
      <td>3782450.0</td>
      <td>3.154336e+11</td>
    </tr>
    <tr>
      <th>153</th>
      <td>2014</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>55776.0</td>
      <td>82.90</td>
      <td>8229629.0</td>
      <td>4.590158e+11</td>
    </tr>
    <tr>
      <th>165</th>
      <td>2014</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>78958.0</td>
      <td>81.90</td>
      <td>5448342.0</td>
      <td>4.301902e+11</td>
    </tr>
    <tr>
      <th>264</th>
      <td>2013</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>136540.0</td>
      <td>80.40</td>
      <td>575841.0</td>
      <td>7.862533e+10</td>
    </tr>
    <tr>
      <th>265</th>
      <td>2013</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88850.0</td>
      <td>81.90</td>
      <td>544721.0</td>
      <td>4.839846e+10</td>
    </tr>
    <tr>
      <th>280</th>
      <td>2013</td>
      <td>europe</td>
      <td>Norway</td>
      <td>63322.0</td>
      <td>81.60</td>
      <td>5077101.0</td>
      <td>3.214922e+11</td>
    </tr>
    <tr>
      <th>312</th>
      <td>2013</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>51656.0</td>
      <td>83.38</td>
      <td>7148571.0</td>
      <td>3.692666e+11</td>
    </tr>
    <tr>
      <th>421</th>
      <td>2013</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>77721.0</td>
      <td>81.70</td>
      <td>5360837.0</td>
      <td>4.166496e+11</td>
    </tr>
    <tr>
      <th>435</th>
      <td>2013</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54983.0</td>
      <td>82.80</td>
      <td>8132674.0</td>
      <td>4.471588e+11</td>
    </tr>
    <tr>
      <th>499</th>
      <td>2012</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>125515.0</td>
      <td>80.19</td>
      <td>562531.0</td>
      <td>7.060608e+10</td>
    </tr>
    <tr>
      <th>500</th>
      <td>2012</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>89153.0</td>
      <td>81.70</td>
      <td>532387.0</td>
      <td>4.746390e+10</td>
    </tr>
    <tr>
      <th>514</th>
      <td>2012</td>
      <td>europe</td>
      <td>Norway</td>
      <td>63620.0</td>
      <td>81.60</td>
      <td>5012007.0</td>
      <td>3.188639e+11</td>
    </tr>
    <tr>
      <th>542</th>
      <td>2012</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>50347.0</td>
      <td>83.20</td>
      <td>7106399.0</td>
      <td>3.577859e+11</td>
    </tr>
    <tr>
      <th>651</th>
      <td>2012</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>75630.0</td>
      <td>81.60</td>
      <td>5270958.0</td>
      <td>3.986426e+11</td>
    </tr>
    <tr>
      <th>665</th>
      <td>2012</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54573.0</td>
      <td>82.70</td>
      <td>8031670.0</td>
      <td>4.383123e+11</td>
    </tr>
    <tr>
      <th>760</th>
      <td>2011</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>50086.0</td>
      <td>83.02</td>
      <td>7065815.0</td>
      <td>3.538984e+11</td>
    </tr>
    <tr>
      <th>776</th>
      <td>2011</td>
      <td>europe</td>
      <td>Norway</td>
      <td>62737.0</td>
      <td>81.10</td>
      <td>4947595.0</td>
      <td>3.103973e+11</td>
    </tr>
    <tr>
      <th>837</th>
      <td>2011</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>91469.0</td>
      <td>81.50</td>
      <td>519941.0</td>
      <td>4.755848e+10</td>
    </tr>
    <tr>
      <th>888</th>
      <td>2011</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>74949.0</td>
      <td>81.50</td>
      <td>5176017.0</td>
      <td>3.879373e+11</td>
    </tr>
    <tr>
      <th>901</th>
      <td>2011</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54551.0</td>
      <td>82.60</td>
      <td>7930421.0</td>
      <td>4.326124e+11</td>
    </tr>
    <tr>
      <th>964</th>
      <td>2010</td>
      <td>europe</td>
      <td>Norway</td>
      <td>62946.0</td>
      <td>81.10</td>
      <td>4885878.0</td>
      <td>3.075465e+11</td>
    </tr>
    <tr>
      <th>1079</th>
      <td>2010</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>91147.0</td>
      <td>81.30</td>
      <td>507889.0</td>
      <td>4.629256e+10</td>
    </tr>
    <tr>
      <th>1127</th>
      <td>2010</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>72056.0</td>
      <td>81.30</td>
      <td>5074252.0</td>
      <td>3.656303e+11</td>
    </tr>
    <tr>
      <th>1139</th>
      <td>2010</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54183.0</td>
      <td>82.30</td>
      <td>7831971.0</td>
      <td>4.243597e+11</td>
    </tr>
    <tr>
      <th>1197</th>
      <td>2009</td>
      <td>europe</td>
      <td>Norway</td>
      <td>63354.0</td>
      <td>80.80</td>
      <td>4827180.0</td>
      <td>3.058212e+11</td>
    </tr>
    <tr>
      <th>1317</th>
      <td>2009</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88284.0</td>
      <td>81.20</td>
      <td>496279.0</td>
      <td>4.381350e+10</td>
    </tr>
    <tr>
      <th>1363</th>
      <td>2009</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>63644.0</td>
      <td>81.00</td>
      <td>4965518.0</td>
      <td>3.160254e+11</td>
    </tr>
    <tr>
      <th>1375</th>
      <td>2009</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>53179.0</td>
      <td>82.00</td>
      <td>7737161.0</td>
      <td>4.114545e+11</td>
    </tr>
    <tr>
      <th>1435</th>
      <td>2008</td>
      <td>europe</td>
      <td>Norway</td>
      <td>65216.0</td>
      <td>80.80</td>
      <td>4771409.0</td>
      <td>3.111722e+11</td>
    </tr>
    <tr>
      <th>1554</th>
      <td>2008</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>95001.0</td>
      <td>81.00</td>
      <td>485105.0</td>
      <td>4.608546e+10</td>
    </tr>
    <tr>
      <th>1603</th>
      <td>2008</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>65991.0</td>
      <td>80.60</td>
      <td>4851109.0</td>
      <td>3.201295e+11</td>
    </tr>
    <tr>
      <th>1615</th>
      <td>2008</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>55020.0</td>
      <td>82.00</td>
      <td>7646113.0</td>
      <td>4.206891e+11</td>
    </tr>
    <tr>
      <th>1686</th>
      <td>2007</td>
      <td>europe</td>
      <td>Norway</td>
      <td>65781.0</td>
      <td>80.60</td>
      <td>4719648.0</td>
      <td>3.104632e+11</td>
    </tr>
    <tr>
      <th>1710</th>
      <td>2007</td>
      <td>europe</td>
      <td>Ireland</td>
      <td>50001.0</td>
      <td>80.10</td>
      <td>4398073.0</td>
      <td>2.199080e+11</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>2007</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>96245.0</td>
      <td>80.60</td>
      <td>474722.0</td>
      <td>4.568962e+10</td>
    </tr>
    <tr>
      <th>1855</th>
      <td>2007</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>68375.0</td>
      <td>80.40</td>
      <td>4732528.0</td>
      <td>3.235866e+11</td>
    </tr>
    <tr>
      <th>1868</th>
      <td>2007</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>54483.0</td>
      <td>81.70</td>
      <td>7560358.0</td>
      <td>4.119110e+11</td>
    </tr>
    <tr>
      <th>1942</th>
      <td>2006</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64573.0</td>
      <td>80.40</td>
      <td>4673070.0</td>
      <td>3.017541e+11</td>
    </tr>
    <tr>
      <th>2060</th>
      <td>2006</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>91810.0</td>
      <td>80.30</td>
      <td>465554.0</td>
      <td>4.274251e+10</td>
    </tr>
    <tr>
      <th>2111</th>
      <td>2006</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>65331.0</td>
      <td>80.20</td>
      <td>4611901.0</td>
      <td>3.013001e+11</td>
    </tr>
    <tr>
      <th>2124</th>
      <td>2006</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>52786.0</td>
      <td>81.50</td>
      <td>7481407.0</td>
      <td>3.949135e+11</td>
    </tr>
    <tr>
      <th>2196</th>
      <td>2005</td>
      <td>europe</td>
      <td>Norway</td>
      <td>63573.0</td>
      <td>80.20</td>
      <td>4632364.0</td>
      <td>2.944933e+11</td>
    </tr>
    <tr>
      <th>2371</th>
      <td>2005</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>51069.0</td>
      <td>81.30</td>
      <td>7410308.0</td>
      <td>3.784370e+11</td>
    </tr>
  </tbody>
</table>
</div>



## 18


```python
df[(df['income'] > 50000) | (df['life_exp'] > 80)]
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>2014</td>
      <td>europe</td>
      <td>Norway</td>
      <td>64020.0</td>
      <td>82.00</td>
      <td>5140311.0</td>
      <td>3.290827e+11</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2014</td>
      <td>europe</td>
      <td>Netherlands</td>
      <td>45281.0</td>
      <td>81.30</td>
      <td>16889356.0</td>
      <td>7.647669e+11</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2014</td>
      <td>europe</td>
      <td>Austria</td>
      <td>43906.0</td>
      <td>81.20</td>
      <td>8633220.0</td>
      <td>3.790502e+11</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2014</td>
      <td>asia</td>
      <td>New Zealand</td>
      <td>33538.0</td>
      <td>81.40</td>
      <td>4566700.0</td>
      <td>1.531580e+11</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2014</td>
      <td>europe</td>
      <td>Malta</td>
      <td>29508.0</td>
      <td>82.00</td>
      <td>425570.0</td>
      <td>1.255772e+10</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>588781.0</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2014</td>
      <td>americas</td>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>80.38</td>
      <td>105110.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2014</td>
      <td>europe</td>
      <td>France</td>
      <td>37218.0</td>
      <td>81.70</td>
      <td>64190638.0</td>
      <td>2.389047e+12</td>
    </tr>
    <tr>
      <th>37</th>
      <td>2014</td>
      <td>europe</td>
      <td>Ireland</td>
      <td>46633.0</td>
      <td>81.60</td>
      <td>4686347.0</td>
      <td>2.185384e+11</td>
    </tr>
    <tr>
      <th>40</th>
      <td>2014</td>
      <td>europe</td>
      <td>Italy</td>
      <td>33078.0</td>
      <td>82.10</td>
      <td>59585668.0</td>
      <td>1.970975e+12</td>
    </tr>
    <tr>
      <th>41</th>
      <td>2014</td>
      <td>asia</td>
      <td>Israel</td>
      <td>31180.0</td>
      <td>81.30</td>
      <td>7941329.0</td>
      <td>2.476106e+11</td>
    </tr>
    <tr>
      <th>43</th>
      <td>2014</td>
      <td>asia</td>
      <td>Japan</td>
      <td>35635.0</td>
      <td>83.10</td>
      <td>128162873.0</td>
      <td>4.567084e+12</td>
    </tr>
    <tr>
      <th>50</th>
      <td>2014</td>
      <td>europe</td>
      <td>Iceland</td>
      <td>41237.0</td>
      <td>83.30</td>
      <td>328459.0</td>
      <td>1.354466e+10</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2014</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>52552.0</td>
      <td>83.56</td>
      <td>7194563.0</td>
      <td>3.780887e+11</td>
    </tr>
    <tr>
      <th>56</th>
      <td>2014</td>
      <td>europe</td>
      <td>Luxembourg</td>
      <td>88203.0</td>
      <td>82.10</td>
      <td>556316.0</td>
      <td>4.906874e+10</td>
    </tr>
    <tr>
      <th>58</th>
      <td>2014</td>
      <td>europe</td>
      <td>Denmark</td>
      <td>42777.0</td>
      <td>80.30</td>
      <td>5663914.0</td>
      <td>2.422852e+11</td>
    </tr>
    <tr>
      <th>68</th>
      <td>2014</td>
      <td>americas</td>
      <td>Canada</td>
      <td>42817.0</td>
      <td>81.70</td>
      <td>35604728.0</td>
      <td>1.524488e+12</td>
    </tr>
    <tr>
      <th>73</th>
      <td>2014</td>
      <td>americas</td>
      <td>Costa Rica</td>
      <td>13713.0</td>
      <td>80.20</td>
      <td>4757575.0</td>
      <td>6.524063e+10</td>
    </tr>
    <tr>
      <th>75</th>
      <td>2014</td>
      <td>asia</td>
      <td>Australia</td>
      <td>43219.0</td>
      <td>82.30</td>
      <td>23474668.0</td>
      <td>1.014552e+12</td>
    </tr>
    <tr>
      <th>76</th>
      <td>2014</td>
      <td>europe</td>
      <td>Germany</td>
      <td>43444.0</td>
      <td>80.70</td>
      <td>81489660.0</td>
      <td>3.540237e+12</td>
    </tr>
    <tr>
      <th>77</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kuwait</td>
      <td>83394.0</td>
      <td>80.20</td>
      <td>3782450.0</td>
      <td>3.154336e+11</td>
    </tr>
    <tr>
      <th>78</th>
      <td>2014</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>72219.0</td>
      <td>77.10</td>
      <td>411704.0</td>
      <td>2.973285e+10</td>
    </tr>
    <tr>
      <th>83</th>
      <td>2014</td>
      <td>europe</td>
      <td>Cyprus</td>
      <td>29673.0</td>
      <td>81.70</td>
      <td>1152309.0</td>
      <td>3.419246e+10</td>
    </tr>
    <tr>
      <th>98</th>
      <td>2014</td>
      <td>europe</td>
      <td>Belgium</td>
      <td>40885.0</td>
      <td>80.50</td>
      <td>11219161.0</td>
      <td>4.586954e+11</td>
    </tr>
    <tr>
      <th>99</th>
      <td>2014</td>
      <td>europe</td>
      <td>Greece</td>
      <td>24502.0</td>
      <td>81.00</td>
      <td>11264726.0</td>
      <td>2.760083e+11</td>
    </tr>
    <tr>
      <th>103</th>
      <td>2014</td>
      <td>europe</td>
      <td>United Kingdom</td>
      <td>37614.0</td>
      <td>80.90</td>
      <td>65015686.0</td>
      <td>2.445500e+12</td>
    </tr>
    <tr>
      <th>112</th>
      <td>2014</td>
      <td>asia</td>
      <td>United Arab Emirates</td>
      <td>60578.0</td>
      <td>75.40</td>
      <td>9070867.0</td>
      <td>5.494950e+11</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2014</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>44929.0</td>
      <td>84.80</td>
      <td>79223.0</td>
      <td>3.559410e+09</td>
    </tr>
    <tr>
      <th>153</th>
      <td>2014</td>
      <td>europe</td>
      <td>Switzerland</td>
      <td>55776.0</td>
      <td>82.90</td>
      <td>8229629.0</td>
      <td>4.590158e+11</td>
    </tr>
    <tr>
      <th>157</th>
      <td>2014</td>
      <td>europe</td>
      <td>Monaco</td>
      <td>61738.0</td>
      <td>NaN</td>
      <td>38132.0</td>
      <td>2.354193e+09</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>11188</th>
      <td>1970</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>158673.0</td>
      <td>67.91</td>
      <td>109514.0</td>
      <td>1.737691e+10</td>
    </tr>
    <tr>
      <th>11218</th>
      <td>1970</td>
      <td>africa</td>
      <td>Libya</td>
      <td>67491.0</td>
      <td>59.01</td>
      <td>2133526.0</td>
      <td>1.439938e+11</td>
    </tr>
    <tr>
      <th>11325</th>
      <td>1969</td>
      <td>asia</td>
      <td>Nauru</td>
      <td>50241.0</td>
      <td>NaN</td>
      <td>6371.0</td>
      <td>3.200854e+08</td>
    </tr>
    <tr>
      <th>11344</th>
      <td>1969</td>
      <td>africa</td>
      <td>Libya</td>
      <td>66299.0</td>
      <td>57.88</td>
      <td>2043818.0</td>
      <td>1.355031e+11</td>
    </tr>
    <tr>
      <th>11395</th>
      <td>1969</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>72988.0</td>
      <td>66.97</td>
      <td>123653.0</td>
      <td>9.025185e+09</td>
    </tr>
    <tr>
      <th>11491</th>
      <td>1969</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>125963.0</td>
      <td>67.29</td>
      <td>100874.0</td>
      <td>1.270639e+10</td>
    </tr>
    <tr>
      <th>11648</th>
      <td>1968</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>71861.0</td>
      <td>66.54</td>
      <td>117950.0</td>
      <td>8.476005e+09</td>
    </tr>
    <tr>
      <th>11685</th>
      <td>1968</td>
      <td>africa</td>
      <td>Libya</td>
      <td>60948.0</td>
      <td>56.69</td>
      <td>1958914.0</td>
      <td>1.193919e+11</td>
    </tr>
    <tr>
      <th>11755</th>
      <td>1968</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>99995.0</td>
      <td>66.64</td>
      <td>93201.0</td>
      <td>9.319634e+09</td>
    </tr>
    <tr>
      <th>11891</th>
      <td>1967</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>70751.0</td>
      <td>66.12</td>
      <td>112494.0</td>
      <td>7.959063e+09</td>
    </tr>
    <tr>
      <th>12000</th>
      <td>1967</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>79381.0</td>
      <td>65.95</td>
      <td>86295.0</td>
      <td>6.850183e+09</td>
    </tr>
    <tr>
      <th>12145</th>
      <td>1966</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>69658.0</td>
      <td>65.67</td>
      <td>107316.0</td>
      <td>7.475418e+09</td>
    </tr>
    <tr>
      <th>12216</th>
      <td>1966</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>63016.0</td>
      <td>65.25</td>
      <td>79844.0</td>
      <td>5.031450e+09</td>
    </tr>
    <tr>
      <th>12326</th>
      <td>1965</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>68582.0</td>
      <td>65.21</td>
      <td>102425.0</td>
      <td>7.024511e+09</td>
    </tr>
    <tr>
      <th>12465</th>
      <td>1965</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>50024.0</td>
      <td>64.53</td>
      <td>73633.0</td>
      <td>3.683417e+09</td>
    </tr>
    <tr>
      <th>12580</th>
      <td>1964</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>67522.0</td>
      <td>64.72</td>
      <td>97848.0</td>
      <td>6.606893e+09</td>
    </tr>
    <tr>
      <th>12913</th>
      <td>1963</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>66479.0</td>
      <td>64.21</td>
      <td>93576.0</td>
      <td>6.220839e+09</td>
    </tr>
    <tr>
      <th>13089</th>
      <td>1962</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>65451.0</td>
      <td>63.67</td>
      <td>89516.0</td>
      <td>5.858912e+09</td>
    </tr>
    <tr>
      <th>13344</th>
      <td>1961</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>64439.0</td>
      <td>63.11</td>
      <td>85596.0</td>
      <td>5.515721e+09</td>
    </tr>
    <tr>
      <th>13596</th>
      <td>1960</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>63442.0</td>
      <td>62.52</td>
      <td>81745.0</td>
      <td>5.186066e+09</td>
    </tr>
    <tr>
      <th>13932</th>
      <td>1959</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>62460.0</td>
      <td>61.93</td>
      <td>77919.0</td>
      <td>4.866821e+09</td>
    </tr>
    <tr>
      <th>14183</th>
      <td>1958</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>61493.0</td>
      <td>61.31</td>
      <td>74150.0</td>
      <td>4.559706e+09</td>
    </tr>
    <tr>
      <th>14444</th>
      <td>1957</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>60541.0</td>
      <td>60.70</td>
      <td>70457.0</td>
      <td>4.265537e+09</td>
    </tr>
    <tr>
      <th>14698</th>
      <td>1956</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>59604.0</td>
      <td>60.07</td>
      <td>66862.0</td>
      <td>3.985243e+09</td>
    </tr>
    <tr>
      <th>14935</th>
      <td>1955</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>58680.0</td>
      <td>59.45</td>
      <td>63420.0</td>
      <td>3.721486e+09</td>
    </tr>
    <tr>
      <th>15196</th>
      <td>1954</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>57771.0</td>
      <td>58.83</td>
      <td>60120.0</td>
      <td>3.473193e+09</td>
    </tr>
    <tr>
      <th>15455</th>
      <td>1953</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>56876.0</td>
      <td>58.22</td>
      <td>56968.0</td>
      <td>3.240112e+09</td>
    </tr>
    <tr>
      <th>15629</th>
      <td>1952</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>55994.0</td>
      <td>57.60</td>
      <td>53927.0</td>
      <td>3.019588e+09</td>
    </tr>
    <tr>
      <th>15951</th>
      <td>1951</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>55126.0</td>
      <td>56.99</td>
      <td>50961.0</td>
      <td>2.809276e+09</td>
    </tr>
    <tr>
      <th>16136</th>
      <td>1950</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>54271.0</td>
      <td>56.68</td>
      <td>48001.0</td>
      <td>2.605062e+09</td>
    </tr>
  </tbody>
</table>
<p>660 rows × 7 columns</p>
</div>



## 19


```python
df['life_exp'].sum() #.dropna().sum()
```




    1840878.89



## 20


```python
df['life_exp'].mean() #.dropna().mean()
```




    42.3765311571997



## 21


```python
df['life_exp'].fillna(value = 0).mean()
```




    33.784413184310814



## 22


```python
df['life_exp'].dropna()
```




    0        70.70
    1        74.30
    3        65.60
    5        74.30
    6        82.00
    7        63.70
    8        77.80
    9        81.30
    10       60.50
    11       79.40
    12       71.10
    13       77.80
    14       81.20
    15       81.40
    16       75.60
    17       69.60
    18       60.10
    19       82.00
    20       60.00
    21       74.50
    22       75.10
    23       60.10
    24       77.00
    25       80.00
    26       76.20
    27       80.61
    28       75.00
    29       56.10
    30       80.38
    31       61.00
             ...  
    54433    23.39
    54435    32.90
    54436    32.30
    54437    32.16
    54438    31.10
    54439    28.30
    54440    24.24
    54441    32.20
    54442    30.40
    54443    28.95
    54444    31.30
    54445    28.20
    54446    28.80
    54447    27.66
    54448    35.00
    54449    24.00
    54450    32.00
    54451    25.30
    54452    36.60
    54453    38.65
    54455    39.41
    54456    32.90
    54457    26.93
    54458    24.30
    54459    32.20
    54460    32.60
    54461    36.10
    54463    33.00
    54464    33.40
    54465    34.75
    Name: life_exp, Length: 43441, dtype: float64



## 23


```python
by_year = df.groupby(by = 'year')
by_year.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="8" halign="left">gross_income</th>
      <th colspan="2" halign="left">income</th>
      <th>...</th>
      <th colspan="2" halign="left">life_exp</th>
      <th colspan="8" halign="left">population</th>
    </tr>
    <tr>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>...</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1800</th>
      <td>201.0</td>
      <td>5.292930e+09</td>
      <td>2.640499e+10</td>
      <td>1016036.0</td>
      <td>7.380000e+07</td>
      <td>4.121721e+08</td>
      <td>1.887270e+09</td>
      <td>3.168499e+11</td>
      <td>201.0</td>
      <td>946.288557</td>
      <td>...</td>
      <td>33.9000</td>
      <td>42.85</td>
      <td>254.0</td>
      <td>4.149630e+06</td>
      <td>2.320847e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>396432.5</td>
      <td>1989821.00</td>
      <td>3.216750e+08</td>
    </tr>
    <tr>
      <th>1801</th>
      <td>201.0</td>
      <td>5.319338e+09</td>
      <td>2.658421e+10</td>
      <td>1016036.0</td>
      <td>7.380000e+07</td>
      <td>4.121721e+08</td>
      <td>1.889360e+09</td>
      <td>3.195427e+11</td>
      <td>201.0</td>
      <td>946.661692</td>
      <td>...</td>
      <td>33.9000</td>
      <td>40.30</td>
      <td>254.0</td>
      <td>4.167524e+06</td>
      <td>2.336951e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>396432.5</td>
      <td>1996964.50</td>
      <td>3.244089e+08</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>201.0</td>
      <td>5.360029e+09</td>
      <td>2.677904e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.121721e+08</td>
      <td>1.889360e+09</td>
      <td>3.222585e+11</td>
      <td>201.0</td>
      <td>949.452736</td>
      <td>...</td>
      <td>33.9000</td>
      <td>44.37</td>
      <td>254.0</td>
      <td>4.185563e+06</td>
      <td>2.353204e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>396432.5</td>
      <td>1998352.00</td>
      <td>3.271659e+08</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>201.0</td>
      <td>5.385297e+09</td>
      <td>2.696226e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.121721e+08</td>
      <td>1.889360e+09</td>
      <td>3.249973e+11</td>
      <td>201.0</td>
      <td>949.194030</td>
      <td>...</td>
      <td>33.8000</td>
      <td>44.84</td>
      <td>254.0</td>
      <td>4.203777e+06</td>
      <td>2.369607e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>396432.5</td>
      <td>1999743.50</td>
      <td>3.299465e+08</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>201.0</td>
      <td>5.422209e+09</td>
      <td>2.715969e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.147769e+08</td>
      <td>1.889360e+09</td>
      <td>3.277593e+11</td>
      <td>201.0</td>
      <td>950.751244</td>
      <td>...</td>
      <td>33.8700</td>
      <td>42.83</td>
      <td>254.0</td>
      <td>4.222136e+06</td>
      <td>2.386161e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>396432.5</td>
      <td>2003416.25</td>
      <td>3.327506e+08</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>201.0</td>
      <td>5.453558e+09</td>
      <td>2.735121e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.201952e+08</td>
      <td>1.889360e+09</td>
      <td>3.305449e+11</td>
      <td>201.0</td>
      <td>951.184080</td>
      <td>...</td>
      <td>33.9000</td>
      <td>44.27</td>
      <td>254.0</td>
      <td>4.240635e+06</td>
      <td>2.402868e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>400674.5</td>
      <td>2007613.25</td>
      <td>3.355786e+08</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>201.0</td>
      <td>5.486458e+09</td>
      <td>2.754437e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.256847e+08</td>
      <td>1.889360e+09</td>
      <td>3.333541e+11</td>
      <td>201.0</td>
      <td>952.328358</td>
      <td>...</td>
      <td>34.0000</td>
      <td>45.82</td>
      <td>254.0</td>
      <td>4.259263e+06</td>
      <td>2.419728e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>406716.0</td>
      <td>2011823.00</td>
      <td>3.384306e+08</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>201.0</td>
      <td>5.524610e+09</td>
      <td>2.775486e+10</td>
      <td>1016036.0</td>
      <td>7.386000e+07</td>
      <td>4.312462e+08</td>
      <td>1.889360e+09</td>
      <td>3.361872e+11</td>
      <td>201.0</td>
      <td>951.980100</td>
      <td>...</td>
      <td>34.0000</td>
      <td>43.56</td>
      <td>254.0</td>
      <td>4.278008e+06</td>
      <td>2.436744e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.413068e+08</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>201.0</td>
      <td>5.541086e+09</td>
      <td>2.794005e+10</td>
      <td>1017870.0</td>
      <td>7.392000e+07</td>
      <td>4.368799e+08</td>
      <td>1.891450e+09</td>
      <td>3.390444e+11</td>
      <td>201.0</td>
      <td>949.084577</td>
      <td>...</td>
      <td>33.8700</td>
      <td>43.55</td>
      <td>254.0</td>
      <td>4.296867e+06</td>
      <td>2.453917e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.442075e+08</td>
    </tr>
    <tr>
      <th>1809</th>
      <td>201.0</td>
      <td>5.579419e+09</td>
      <td>2.814583e+10</td>
      <td>1017870.0</td>
      <td>7.392000e+07</td>
      <td>4.425873e+08</td>
      <td>1.891450e+09</td>
      <td>3.419259e+11</td>
      <td>201.0</td>
      <td>950.144279</td>
      <td>...</td>
      <td>33.8000</td>
      <td>41.74</td>
      <td>254.0</td>
      <td>4.315812e+06</td>
      <td>2.471247e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.471329e+08</td>
    </tr>
    <tr>
      <th>1810</th>
      <td>201.0</td>
      <td>5.612397e+09</td>
      <td>2.833510e+10</td>
      <td>1017870.0</td>
      <td>7.392000e+07</td>
      <td>4.437655e+08</td>
      <td>1.891450e+09</td>
      <td>3.448319e+11</td>
      <td>201.0</td>
      <td>954.069652</td>
      <td>...</td>
      <td>33.9000</td>
      <td>43.14</td>
      <td>254.0</td>
      <td>4.334875e+06</td>
      <td>2.488738e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.500831e+08</td>
    </tr>
    <tr>
      <th>1811</th>
      <td>201.0</td>
      <td>5.633909e+09</td>
      <td>2.851703e+10</td>
      <td>1017870.0</td>
      <td>7.473074e+07</td>
      <td>4.437655e+08</td>
      <td>1.891450e+09</td>
      <td>3.477625e+11</td>
      <td>201.0</td>
      <td>954.900498</td>
      <td>...</td>
      <td>33.9000</td>
      <td>40.09</td>
      <td>254.0</td>
      <td>4.354265e+06</td>
      <td>2.506392e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.530584e+08</td>
    </tr>
    <tr>
      <th>1812</th>
      <td>201.0</td>
      <td>5.648213e+09</td>
      <td>2.870443e+10</td>
      <td>1017870.0</td>
      <td>7.478204e+07</td>
      <td>4.437655e+08</td>
      <td>1.899714e+09</td>
      <td>3.507181e+11</td>
      <td>201.0</td>
      <td>951.721393</td>
      <td>...</td>
      <td>33.9000</td>
      <td>43.46</td>
      <td>254.0</td>
      <td>4.373879e+06</td>
      <td>2.524209e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.560590e+08</td>
    </tr>
    <tr>
      <th>1813</th>
      <td>201.0</td>
      <td>5.692809e+09</td>
      <td>2.893148e+10</td>
      <td>1017870.0</td>
      <td>7.478204e+07</td>
      <td>4.437655e+08</td>
      <td>1.909149e+09</td>
      <td>3.536988e+11</td>
      <td>201.0</td>
      <td>951.910448</td>
      <td>...</td>
      <td>33.8700</td>
      <td>43.04</td>
      <td>254.0</td>
      <td>4.393649e+06</td>
      <td>2.542189e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.590850e+08</td>
    </tr>
    <tr>
      <th>1814</th>
      <td>201.0</td>
      <td>5.719493e+09</td>
      <td>2.912896e+10</td>
      <td>1017870.0</td>
      <td>7.478204e+07</td>
      <td>4.437655e+08</td>
      <td>1.918627e+09</td>
      <td>3.567048e+11</td>
      <td>201.0</td>
      <td>951.890547</td>
      <td>...</td>
      <td>34.0000</td>
      <td>41.74</td>
      <td>254.0</td>
      <td>4.413575e+06</td>
      <td>2.560333e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.621368e+08</td>
    </tr>
    <tr>
      <th>1815</th>
      <td>201.0</td>
      <td>5.774900e+09</td>
      <td>2.935744e+10</td>
      <td>1017870.0</td>
      <td>7.486376e+07</td>
      <td>4.437655e+08</td>
      <td>1.928149e+09</td>
      <td>3.597363e+11</td>
      <td>201.0</td>
      <td>958.572139</td>
      <td>...</td>
      <td>34.0500</td>
      <td>45.58</td>
      <td>254.0</td>
      <td>4.433686e+06</td>
      <td>2.578645e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.652145e+08</td>
    </tr>
    <tr>
      <th>1816</th>
      <td>201.0</td>
      <td>5.779540e+09</td>
      <td>2.953098e+10</td>
      <td>1017870.0</td>
      <td>7.486376e+07</td>
      <td>4.437655e+08</td>
      <td>1.937714e+09</td>
      <td>3.627936e+11</td>
      <td>201.0</td>
      <td>956.601990</td>
      <td>...</td>
      <td>34.0000</td>
      <td>46.33</td>
      <td>254.0</td>
      <td>4.453991e+06</td>
      <td>2.597123e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.683184e+08</td>
    </tr>
    <tr>
      <th>1817</th>
      <td>201.0</td>
      <td>5.814422e+09</td>
      <td>2.974161e+10</td>
      <td>1017870.0</td>
      <td>7.486376e+07</td>
      <td>4.439236e+08</td>
      <td>1.947323e+09</td>
      <td>3.658770e+11</td>
      <td>201.0</td>
      <td>957.452736</td>
      <td>...</td>
      <td>34.0500</td>
      <td>48.87</td>
      <td>254.0</td>
      <td>4.474464e+06</td>
      <td>2.615771e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.714487e+08</td>
    </tr>
    <tr>
      <th>1818</th>
      <td>201.0</td>
      <td>5.862469e+09</td>
      <td>2.997480e+10</td>
      <td>1017870.0</td>
      <td>7.486376e+07</td>
      <td>4.439236e+08</td>
      <td>1.956977e+09</td>
      <td>3.689865e+11</td>
      <td>201.0</td>
      <td>959.199005</td>
      <td>...</td>
      <td>34.0500</td>
      <td>46.75</td>
      <td>254.0</td>
      <td>4.495060e+06</td>
      <td>2.634591e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.746056e+08</td>
    </tr>
    <tr>
      <th>1819</th>
      <td>201.0</td>
      <td>5.884003e+09</td>
      <td>3.017585e+10</td>
      <td>1017870.0</td>
      <td>7.486376e+07</td>
      <td>4.439236e+08</td>
      <td>1.966674e+09</td>
      <td>3.721224e+11</td>
      <td>201.0</td>
      <td>958.338308</td>
      <td>...</td>
      <td>34.0500</td>
      <td>45.78</td>
      <td>254.0</td>
      <td>4.515803e+06</td>
      <td>2.653582e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.777892e+08</td>
    </tr>
    <tr>
      <th>1820</th>
      <td>202.0</td>
      <td>5.915726e+09</td>
      <td>3.034552e+10</td>
      <td>1019704.0</td>
      <td>7.739645e+07</td>
      <td>4.494558e+08</td>
      <td>1.964314e+09</td>
      <td>3.752850e+11</td>
      <td>202.0</td>
      <td>963.356436</td>
      <td>...</td>
      <td>34.0500</td>
      <td>46.96</td>
      <td>254.0</td>
      <td>4.536700e+06</td>
      <td>2.672748e+07</td>
      <td>0.0</td>
      <td>31750.00</td>
      <td>407163.0</td>
      <td>2012025.50</td>
      <td>3.810000e+08</td>
    </tr>
    <tr>
      <th>1821</th>
      <td>202.0</td>
      <td>5.988010e+09</td>
      <td>3.058230e+10</td>
      <td>1027278.0</td>
      <td>7.885895e+07</td>
      <td>4.557471e+08</td>
      <td>1.986636e+09</td>
      <td>3.779558e+11</td>
      <td>202.0</td>
      <td>969.821782</td>
      <td>...</td>
      <td>34.0000</td>
      <td>44.69</td>
      <td>254.0</td>
      <td>4.568149e+06</td>
      <td>2.690429e+07</td>
      <td>0.0</td>
      <td>32223.25</td>
      <td>409024.0</td>
      <td>2006324.50</td>
      <td>3.837115e+08</td>
    </tr>
    <tr>
      <th>1822</th>
      <td>202.0</td>
      <td>6.025950e+09</td>
      <td>3.075911e+10</td>
      <td>1036167.0</td>
      <td>8.043973e+07</td>
      <td>4.601013e+08</td>
      <td>1.998008e+09</td>
      <td>3.806457e+11</td>
      <td>202.0</td>
      <td>973.980198</td>
      <td>...</td>
      <td>34.0500</td>
      <td>48.39</td>
      <td>254.0</td>
      <td>4.599823e+06</td>
      <td>2.708243e+07</td>
      <td>0.0</td>
      <td>32706.25</td>
      <td>410902.0</td>
      <td>2011561.00</td>
      <td>3.864423e+08</td>
    </tr>
    <tr>
      <th>1823</th>
      <td>202.0</td>
      <td>6.087423e+09</td>
      <td>3.098333e+10</td>
      <td>1045656.0</td>
      <td>8.196193e+07</td>
      <td>4.612588e+08</td>
      <td>2.007517e+09</td>
      <td>3.833546e+11</td>
      <td>202.0</td>
      <td>979.663366</td>
      <td>...</td>
      <td>34.0500</td>
      <td>48.76</td>
      <td>254.0</td>
      <td>4.631721e+06</td>
      <td>2.726180e+07</td>
      <td>0.0</td>
      <td>33199.00</td>
      <td>413570.5</td>
      <td>2019788.25</td>
      <td>3.891925e+08</td>
    </tr>
    <tr>
      <th>1824</th>
      <td>202.0</td>
      <td>6.158582e+09</td>
      <td>3.121809e+10</td>
      <td>1053326.0</td>
      <td>8.354080e+07</td>
      <td>4.672911e+08</td>
      <td>2.016392e+09</td>
      <td>3.860829e+11</td>
      <td>202.0</td>
      <td>985.866337</td>
      <td>...</td>
      <td>34.0500</td>
      <td>47.64</td>
      <td>254.0</td>
      <td>4.663854e+06</td>
      <td>2.744243e+07</td>
      <td>0.0</td>
      <td>33702.25</td>
      <td>417295.0</td>
      <td>2029954.00</td>
      <td>3.919623e+08</td>
    </tr>
    <tr>
      <th>1825</th>
      <td>202.0</td>
      <td>6.218656e+09</td>
      <td>3.143855e+10</td>
      <td>1062892.0</td>
      <td>8.519018e+07</td>
      <td>4.731403e+08</td>
      <td>2.026839e+09</td>
      <td>3.888305e+11</td>
      <td>202.0</td>
      <td>990.945545</td>
      <td>...</td>
      <td>34.0000</td>
      <td>49.23</td>
      <td>254.0</td>
      <td>4.696225e+06</td>
      <td>2.762437e+07</td>
      <td>0.0</td>
      <td>34216.75</td>
      <td>421053.0</td>
      <td>2056508.00</td>
      <td>3.947518e+08</td>
    </tr>
    <tr>
      <th>1826</th>
      <td>202.0</td>
      <td>6.272059e+09</td>
      <td>3.164564e+10</td>
      <td>1072500.0</td>
      <td>8.679417e+07</td>
      <td>4.790571e+08</td>
      <td>2.041087e+09</td>
      <td>3.915978e+11</td>
      <td>202.0</td>
      <td>995.668317</td>
      <td>...</td>
      <td>34.0000</td>
      <td>47.63</td>
      <td>254.0</td>
      <td>4.728530e+06</td>
      <td>2.780740e+07</td>
      <td>0.0</td>
      <td>34741.75</td>
      <td>424845.0</td>
      <td>2085845.75</td>
      <td>3.975612e+08</td>
    </tr>
    <tr>
      <th>1827</th>
      <td>202.0</td>
      <td>6.347531e+09</td>
      <td>3.189399e+10</td>
      <td>1082150.0</td>
      <td>8.837244e+07</td>
      <td>4.854224e+08</td>
      <td>2.070965e+09</td>
      <td>3.943847e+11</td>
      <td>202.0</td>
      <td>1002.648515</td>
      <td>...</td>
      <td>34.0000</td>
      <td>48.38</td>
      <td>254.0</td>
      <td>4.760875e+06</td>
      <td>2.799161e+07</td>
      <td>0.0</td>
      <td>35277.25</td>
      <td>428671.0</td>
      <td>2108742.25</td>
      <td>4.003905e+08</td>
    </tr>
    <tr>
      <th>1828</th>
      <td>202.0</td>
      <td>6.380584e+09</td>
      <td>3.207201e+10</td>
      <td>1089953.0</td>
      <td>8.989200e+07</td>
      <td>4.914802e+08</td>
      <td>2.103349e+09</td>
      <td>3.971914e+11</td>
      <td>202.0</td>
      <td>1007.316832</td>
      <td>...</td>
      <td>34.0000</td>
      <td>46.22</td>
      <td>254.0</td>
      <td>4.793402e+06</td>
      <td>2.817719e+07</td>
      <td>0.0</td>
      <td>35824.75</td>
      <td>432531.0</td>
      <td>2115344.50</td>
      <td>4.032400e+08</td>
    </tr>
    <tr>
      <th>1829</th>
      <td>202.0</td>
      <td>6.448246e+09</td>
      <td>3.233586e+10</td>
      <td>1099100.0</td>
      <td>9.047827e+07</td>
      <td>4.979955e+08</td>
      <td>2.123043e+09</td>
      <td>4.004243e+11</td>
      <td>202.0</td>
      <td>1012.386139</td>
      <td>...</td>
      <td>34.0000</td>
      <td>46.29</td>
      <td>254.0</td>
      <td>4.826018e+06</td>
      <td>2.836403e+07</td>
      <td>0.0</td>
      <td>36383.50</td>
      <td>436426.5</td>
      <td>2121705.75</td>
      <td>4.061098e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1985</th>
      <td>202.0</td>
      <td>2.004337e+11</td>
      <td>6.820986e+11</td>
      <td>16305250.0</td>
      <td>4.827679e+09</td>
      <td>2.156817e+10</td>
      <td>1.273384e+11</td>
      <td>7.962850e+12</td>
      <td>202.0</td>
      <td>12104.945545</td>
      <td>...</td>
      <td>71.6825</td>
      <td>77.85</td>
      <td>254.0</td>
      <td>2.126360e+07</td>
      <td>8.795424e+07</td>
      <td>62.0</td>
      <td>198355.75</td>
      <td>3563677.5</td>
      <td>10638734.50</td>
      <td>1.070863e+09</td>
    </tr>
    <tr>
      <th>1986</th>
      <td>202.0</td>
      <td>2.068168e+11</td>
      <td>7.058485e+11</td>
      <td>16111974.0</td>
      <td>5.018095e+09</td>
      <td>2.187766e+10</td>
      <td>1.284643e+11</td>
      <td>8.240811e+12</td>
      <td>202.0</td>
      <td>12013.420792</td>
      <td>...</td>
      <td>72.1925</td>
      <td>78.38</td>
      <td>254.0</td>
      <td>2.163641e+07</td>
      <td>8.960726e+07</td>
      <td>63.0</td>
      <td>205010.75</td>
      <td>3582701.0</td>
      <td>10983463.25</td>
      <td>1.090348e+09</td>
    </tr>
    <tr>
      <th>1987</th>
      <td>202.0</td>
      <td>2.137740e+11</td>
      <td>7.302445e+11</td>
      <td>17551800.0</td>
      <td>5.275062e+09</td>
      <td>2.221330e+10</td>
      <td>1.362656e+11</td>
      <td>8.536829e+12</td>
      <td>202.0</td>
      <td>12212.856436</td>
      <td>...</td>
      <td>72.2750</td>
      <td>78.63</td>
      <td>254.0</td>
      <td>2.201880e+07</td>
      <td>9.133629e+07</td>
      <td>63.0</td>
      <td>211748.50</td>
      <td>3599544.0</td>
      <td>11325206.00</td>
      <td>1.111342e+09</td>
    </tr>
    <tr>
      <th>1988</th>
      <td>202.0</td>
      <td>2.218612e+11</td>
      <td>7.611096e+11</td>
      <td>19178397.0</td>
      <td>5.529990e+09</td>
      <td>2.311063e+10</td>
      <td>1.378744e+11</td>
      <td>8.901035e+12</td>
      <td>202.0</td>
      <td>12351.866337</td>
      <td>...</td>
      <td>72.7150</td>
      <td>78.54</td>
      <td>254.0</td>
      <td>2.240565e+07</td>
      <td>9.309351e+07</td>
      <td>64.0</td>
      <td>218528.25</td>
      <td>3620209.0</td>
      <td>11534158.00</td>
      <td>1.132866e+09</td>
    </tr>
    <tr>
      <th>1989</th>
      <td>202.0</td>
      <td>2.286743e+11</td>
      <td>7.868453e+11</td>
      <td>18627654.0</td>
      <td>5.706030e+09</td>
      <td>2.349111e+10</td>
      <td>1.445178e+11</td>
      <td>9.211669e+12</td>
      <td>202.0</td>
      <td>12640.628713</td>
      <td>...</td>
      <td>73.1275</td>
      <td>78.97</td>
      <td>254.0</td>
      <td>2.278707e+07</td>
      <td>9.480619e+07</td>
      <td>64.0</td>
      <td>225324.75</td>
      <td>3684465.0</td>
      <td>11836241.50</td>
      <td>1.153566e+09</td>
    </tr>
    <tr>
      <th>1990</th>
      <td>203.0</td>
      <td>2.321704e+11</td>
      <td>7.974999e+11</td>
      <td>21328107.0</td>
      <td>5.900317e+09</td>
      <td>2.512703e+10</td>
      <td>1.402420e+11</td>
      <td>9.359265e+12</td>
      <td>203.0</td>
      <td>12814.029557</td>
      <td>...</td>
      <td>73.3000</td>
      <td>81.70</td>
      <td>254.0</td>
      <td>2.316234e+07</td>
      <td>9.644211e+07</td>
      <td>65.0</td>
      <td>231172.00</td>
      <td>3741487.0</td>
      <td>12263094.00</td>
      <td>1.172445e+09</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>203.0</td>
      <td>2.344332e+11</td>
      <td>8.007441e+11</td>
      <td>22098373.0</td>
      <td>5.960926e+09</td>
      <td>2.420966e+10</td>
      <td>1.327423e+11</td>
      <td>9.317545e+12</td>
      <td>203.0</td>
      <td>12557.497537</td>
      <td>...</td>
      <td>73.4275</td>
      <td>81.80</td>
      <td>254.0</td>
      <td>2.353319e+07</td>
      <td>9.797670e+07</td>
      <td>64.0</td>
      <td>236721.50</td>
      <td>3835728.0</td>
      <td>12788916.25</td>
      <td>1.189184e+09</td>
    </tr>
    <tr>
      <th>1992</th>
      <td>203.0</td>
      <td>2.382744e+11</td>
      <td>8.182934e+11</td>
      <td>22736064.0</td>
      <td>5.945198e+09</td>
      <td>2.474152e+10</td>
      <td>1.322022e+11</td>
      <td>9.608451e+12</td>
      <td>203.0</td>
      <td>12622.561576</td>
      <td>...</td>
      <td>73.5550</td>
      <td>81.90</td>
      <td>254.0</td>
      <td>2.389015e+07</td>
      <td>9.941645e+07</td>
      <td>63.0</td>
      <td>242180.25</td>
      <td>3970762.5</td>
      <td>13290958.50</td>
      <td>1.204004e+09</td>
    </tr>
    <tr>
      <th>1993</th>
      <td>203.0</td>
      <td>2.425276e+11</td>
      <td>8.350830e+11</td>
      <td>23677416.0</td>
      <td>5.873835e+09</td>
      <td>2.501212e+10</td>
      <td>1.308951e+11</td>
      <td>9.840204e+12</td>
      <td>203.0</td>
      <td>12655.995074</td>
      <td>...</td>
      <td>73.6425</td>
      <td>82.20</td>
      <td>254.0</td>
      <td>2.423275e+07</td>
      <td>1.007730e+08</td>
      <td>63.0</td>
      <td>247508.25</td>
      <td>4076462.5</td>
      <td>13817683.75</td>
      <td>1.217129e+09</td>
    </tr>
    <tr>
      <th>1994</th>
      <td>203.0</td>
      <td>2.498521e+11</td>
      <td>8.643071e+11</td>
      <td>26090410.0</td>
      <td>5.221698e+09</td>
      <td>2.597987e+10</td>
      <td>1.401603e+11</td>
      <td>1.021854e+13</td>
      <td>203.0</td>
      <td>12885.719212</td>
      <td>...</td>
      <td>73.6550</td>
      <td>82.30</td>
      <td>254.0</td>
      <td>2.456898e+07</td>
      <td>1.020736e+08</td>
      <td>62.0</td>
      <td>252328.50</td>
      <td>4139370.5</td>
      <td>14089444.50</td>
      <td>1.228992e+09</td>
    </tr>
    <tr>
      <th>1995</th>
      <td>203.0</td>
      <td>2.581019e+11</td>
      <td>8.896481e+11</td>
      <td>24791780.0</td>
      <td>5.498185e+09</td>
      <td>2.581441e+10</td>
      <td>1.512743e+11</td>
      <td>1.048715e+13</td>
      <td>203.0</td>
      <td>13171.694581</td>
      <td>...</td>
      <td>74.0000</td>
      <td>82.60</td>
      <td>254.0</td>
      <td>2.490143e+07</td>
      <td>1.033395e+08</td>
      <td>61.0</td>
      <td>257965.25</td>
      <td>4240932.0</td>
      <td>14491988.00</td>
      <td>1.239940e+09</td>
    </tr>
    <tr>
      <th>1996</th>
      <td>203.0</td>
      <td>2.680382e+11</td>
      <td>9.234362e+11</td>
      <td>23278840.0</td>
      <td>6.003650e+09</td>
      <td>2.615114e+10</td>
      <td>1.546490e+11</td>
      <td>1.088681e+13</td>
      <td>203.0</td>
      <td>13469.684729</td>
      <td>...</td>
      <td>74.2375</td>
      <td>82.80</td>
      <td>254.0</td>
      <td>2.522809e+07</td>
      <td>1.045719e+08</td>
      <td>60.0</td>
      <td>264566.50</td>
      <td>4284847.0</td>
      <td>14935258.25</td>
      <td>1.249981e+09</td>
    </tr>
    <tr>
      <th>1997</th>
      <td>203.0</td>
      <td>2.788527e+11</td>
      <td>9.628757e+11</td>
      <td>25576689.0</td>
      <td>6.315659e+09</td>
      <td>2.747283e+10</td>
      <td>1.676497e+11</td>
      <td>1.137857e+13</td>
      <td>203.0</td>
      <td>13948.665025</td>
      <td>...</td>
      <td>74.5000</td>
      <td>83.10</td>
      <td>254.0</td>
      <td>2.554911e+07</td>
      <td>1.057677e+08</td>
      <td>60.0</td>
      <td>268386.00</td>
      <td>4295193.0</td>
      <td>15378853.50</td>
      <td>1.259067e+09</td>
    </tr>
    <tr>
      <th>1998</th>
      <td>203.0</td>
      <td>2.855597e+11</td>
      <td>9.985362e+11</td>
      <td>29518632.0</td>
      <td>6.500016e+09</td>
      <td>2.828744e+10</td>
      <td>1.696848e+11</td>
      <td>1.189407e+13</td>
      <td>203.0</td>
      <td>14220.857143</td>
      <td>...</td>
      <td>74.8000</td>
      <td>83.30</td>
      <td>254.0</td>
      <td>2.586722e+07</td>
      <td>1.069367e+08</td>
      <td>59.0</td>
      <td>270728.50</td>
      <td>4303465.0</td>
      <td>15577737.00</td>
      <td>1.267442e+09</td>
    </tr>
    <tr>
      <th>1999</th>
      <td>203.0</td>
      <td>2.956431e+11</td>
      <td>1.042445e+12</td>
      <td>29053605.0</td>
      <td>6.651757e+09</td>
      <td>2.938217e+10</td>
      <td>1.789930e+11</td>
      <td>1.245761e+13</td>
      <td>203.0</td>
      <td>14442.221675</td>
      <td>...</td>
      <td>75.1000</td>
      <td>83.50</td>
      <td>254.0</td>
      <td>2.618334e+07</td>
      <td>1.080890e+08</td>
      <td>59.0</td>
      <td>275330.50</td>
      <td>4331038.0</td>
      <td>15795686.00</td>
      <td>1.275407e+09</td>
    </tr>
    <tr>
      <th>2000</th>
      <td>203.0</td>
      <td>3.093815e+11</td>
      <td>1.087941e+12</td>
      <td>28862880.0</td>
      <td>7.209547e+09</td>
      <td>2.994950e+10</td>
      <td>1.915955e+11</td>
      <td>1.296726e+13</td>
      <td>203.0</td>
      <td>14905.482759</td>
      <td>...</td>
      <td>75.2000</td>
      <td>83.70</td>
      <td>254.0</td>
      <td>2.650043e+07</td>
      <td>1.092328e+08</td>
      <td>58.0</td>
      <td>280396.75</td>
      <td>4314580.5</td>
      <td>15886342.50</td>
      <td>1.283199e+09</td>
    </tr>
    <tr>
      <th>2001</th>
      <td>203.0</td>
      <td>3.167417e+11</td>
      <td>1.107890e+12</td>
      <td>29458664.0</td>
      <td>7.201082e+09</td>
      <td>3.081004e+10</td>
      <td>1.939266e+11</td>
      <td>1.309694e+13</td>
      <td>203.0</td>
      <td>15068.620690</td>
      <td>...</td>
      <td>75.4000</td>
      <td>83.90</td>
      <td>254.0</td>
      <td>2.681894e+07</td>
      <td>1.103727e+08</td>
      <td>56.0</td>
      <td>283937.00</td>
      <td>4296792.5</td>
      <td>16145086.00</td>
      <td>1.290938e+09</td>
    </tr>
    <tr>
      <th>2002</th>
      <td>203.0</td>
      <td>3.255249e+11</td>
      <td>1.135496e+12</td>
      <td>31997835.0</td>
      <td>7.557211e+09</td>
      <td>3.097617e+10</td>
      <td>2.043236e+11</td>
      <td>1.333083e+13</td>
      <td>203.0</td>
      <td>15250.655172</td>
      <td>...</td>
      <td>75.7000</td>
      <td>84.10</td>
      <td>254.0</td>
      <td>2.713840e+07</td>
      <td>1.115101e+08</td>
      <td>55.0</td>
      <td>287582.00</td>
      <td>4286217.5</td>
      <td>16189150.75</td>
      <td>1.298647e+09</td>
    </tr>
    <tr>
      <th>2003</th>
      <td>203.0</td>
      <td>3.375965e+11</td>
      <td>1.176679e+12</td>
      <td>31156730.0</td>
      <td>7.822934e+09</td>
      <td>3.232697e+10</td>
      <td>2.023383e+11</td>
      <td>1.370671e+13</td>
      <td>203.0</td>
      <td>15587.847291</td>
      <td>...</td>
      <td>75.8000</td>
      <td>84.20</td>
      <td>254.0</td>
      <td>2.746062e+07</td>
      <td>1.126471e+08</td>
      <td>53.0</td>
      <td>291516.25</td>
      <td>4319120.5</td>
      <td>16446234.00</td>
      <td>1.306344e+09</td>
    </tr>
    <tr>
      <th>2004</th>
      <td>203.0</td>
      <td>3.556785e+11</td>
      <td>1.230621e+12</td>
      <td>30958326.0</td>
      <td>8.135102e+09</td>
      <td>3.418822e+10</td>
      <td>2.266498e+11</td>
      <td>1.421653e+13</td>
      <td>203.0</td>
      <td>16248.192118</td>
      <td>...</td>
      <td>76.0000</td>
      <td>84.10</td>
      <td>254.0</td>
      <td>2.778648e+07</td>
      <td>1.137834e+08</td>
      <td>52.0</td>
      <td>295933.75</td>
      <td>4376980.0</td>
      <td>16791106.25</td>
      <td>1.314007e+09</td>
    </tr>
    <tr>
      <th>2005</th>
      <td>203.0</td>
      <td>3.724431e+11</td>
      <td>1.286295e+12</td>
      <td>30030865.0</td>
      <td>8.555448e+09</td>
      <td>3.499570e+10</td>
      <td>2.404289e+11</td>
      <td>1.468623e+13</td>
      <td>203.0</td>
      <td>16677.280788</td>
      <td>...</td>
      <td>76.6000</td>
      <td>84.30</td>
      <td>254.0</td>
      <td>2.811636e+07</td>
      <td>1.149187e+08</td>
      <td>50.0</td>
      <td>300943.25</td>
      <td>4488794.5</td>
      <td>17157385.75</td>
      <td>1.321623e+09</td>
    </tr>
    <tr>
      <th>2006</th>
      <td>203.0</td>
      <td>3.926470e+11</td>
      <td>1.346860e+12</td>
      <td>30897576.0</td>
      <td>9.065085e+09</td>
      <td>3.853406e+10</td>
      <td>2.579139e+11</td>
      <td>1.506977e+13</td>
      <td>203.0</td>
      <td>17291.788177</td>
      <td>...</td>
      <td>76.7000</td>
      <td>84.40</td>
      <td>254.0</td>
      <td>2.845033e+07</td>
      <td>1.160532e+08</td>
      <td>50.0</td>
      <td>306638.75</td>
      <td>4624341.0</td>
      <td>17589206.50</td>
      <td>1.329209e+09</td>
    </tr>
    <tr>
      <th>2007</th>
      <td>203.0</td>
      <td>4.140874e+11</td>
      <td>1.412326e+12</td>
      <td>33084890.0</td>
      <td>9.570694e+09</td>
      <td>4.181720e+10</td>
      <td>2.706306e+11</td>
      <td>1.533366e+13</td>
      <td>203.0</td>
      <td>17871.660099</td>
      <td>...</td>
      <td>76.9250</td>
      <td>84.50</td>
      <td>254.0</td>
      <td>2.878812e+07</td>
      <td>1.171867e+08</td>
      <td>50.0</td>
      <td>312917.50</td>
      <td>4726088.0</td>
      <td>18106119.75</td>
      <td>1.336801e+09</td>
    </tr>
    <tr>
      <th>2008</th>
      <td>203.0</td>
      <td>4.259501e+11</td>
      <td>1.446869e+12</td>
      <td>35983200.0</td>
      <td>1.050325e+10</td>
      <td>4.550102e+10</td>
      <td>2.802367e+11</td>
      <td>1.528520e+13</td>
      <td>203.0</td>
      <td>17965.694581</td>
      <td>...</td>
      <td>77.1500</td>
      <td>84.60</td>
      <td>254.0</td>
      <td>2.912917e+07</td>
      <td>1.183166e+08</td>
      <td>50.0</td>
      <td>319426.50</td>
      <td>4811259.0</td>
      <td>18639928.75</td>
      <td>1.344415e+09</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>202.0</td>
      <td>4.272031e+11</td>
      <td>1.461693e+12</td>
      <td>34653679.0</td>
      <td>1.065184e+10</td>
      <td>4.393957e+10</td>
      <td>2.820749e+11</td>
      <td>1.486246e+13</td>
      <td>203.0</td>
      <td>17202.374384</td>
      <td>...</td>
      <td>77.4250</td>
      <td>84.60</td>
      <td>236.0</td>
      <td>2.912601e+07</td>
      <td>1.225329e+08</td>
      <td>50.0</td>
      <td>354767.25</td>
      <td>4528163.5</td>
      <td>17480216.75</td>
      <td>1.352068e+09</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>202.0</td>
      <td>4.498648e+11</td>
      <td>1.546089e+12</td>
      <td>33930882.0</td>
      <td>1.128660e+10</td>
      <td>4.905857e+10</td>
      <td>2.916592e+11</td>
      <td>1.523855e+13</td>
      <td>203.0</td>
      <td>17559.950739</td>
      <td>...</td>
      <td>77.6500</td>
      <td>84.70</td>
      <td>236.0</td>
      <td>2.948360e+07</td>
      <td>1.236949e+08</td>
      <td>50.0</td>
      <td>363591.25</td>
      <td>4586104.0</td>
      <td>17737639.25</td>
      <td>1.359755e+09</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>202.0</td>
      <td>4.680519e+11</td>
      <td>1.619460e+12</td>
      <td>37070464.0</td>
      <td>1.170256e+10</td>
      <td>5.098830e+10</td>
      <td>2.982631e+11</td>
      <td>1.548445e+13</td>
      <td>204.0</td>
      <td>18019.333333</td>
      <td>...</td>
      <td>77.8250</td>
      <td>84.70</td>
      <td>231.0</td>
      <td>3.048871e+07</td>
      <td>1.261147e+08</td>
      <td>796.0</td>
      <td>434907.00</td>
      <td>5174061.0</td>
      <td>20303992.00</td>
      <td>1.367480e+09</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>202.0</td>
      <td>4.838351e+11</td>
      <td>1.691496e+12</td>
      <td>37419525.0</td>
      <td>1.190010e+10</td>
      <td>5.508329e+10</td>
      <td>2.823486e+11</td>
      <td>1.583879e+13</td>
      <td>203.0</td>
      <td>18127.674877</td>
      <td>...</td>
      <td>78.1250</td>
      <td>84.70</td>
      <td>231.0</td>
      <td>3.085723e+07</td>
      <td>1.272596e+08</td>
      <td>804.0</td>
      <td>436195.50</td>
      <td>5267839.0</td>
      <td>20295978.00</td>
      <td>1.375199e+09</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>202.0</td>
      <td>5.000853e+11</td>
      <td>1.768834e+12</td>
      <td>38169432.0</td>
      <td>1.263909e+10</td>
      <td>5.706387e+10</td>
      <td>2.935097e+11</td>
      <td>1.632387e+13</td>
      <td>203.0</td>
      <td>18305.502463</td>
      <td>...</td>
      <td>78.3000</td>
      <td>84.80</td>
      <td>231.0</td>
      <td>3.122610e+07</td>
      <td>1.283877e+08</td>
      <td>801.0</td>
      <td>437292.00</td>
      <td>5360837.0</td>
      <td>19938671.00</td>
      <td>1.382793e+09</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>202.0</td>
      <td>5.166226e+11</td>
      <td>1.850280e+12</td>
      <td>38701584.0</td>
      <td>1.334583e+10</td>
      <td>5.982129e+10</td>
      <td>3.126064e+11</td>
      <td>1.752790e+13</td>
      <td>203.0</td>
      <td>18628.310345</td>
      <td>...</td>
      <td>78.4000</td>
      <td>84.80</td>
      <td>231.0</td>
      <td>3.159399e+07</td>
      <td>1.294970e+08</td>
      <td>800.0</td>
      <td>438227.00</td>
      <td>5448342.0</td>
      <td>19587913.00</td>
      <td>1.390110e+09</td>
    </tr>
  </tbody>
</table>
<p>215 rows × 32 columns</p>
</div>



## 24


```python
by_year['income'].describe()
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1800</th>
      <td>201.0</td>
      <td>946.288557</td>
      <td>502.228769</td>
      <td>350.0</td>
      <td>608.00</td>
      <td>850.0</td>
      <td>1097.00</td>
      <td>4235.0</td>
    </tr>
    <tr>
      <th>1801</th>
      <td>201.0</td>
      <td>946.661692</td>
      <td>500.413744</td>
      <td>350.0</td>
      <td>608.00</td>
      <td>852.0</td>
      <td>1101.00</td>
      <td>4161.0</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>201.0</td>
      <td>949.452736</td>
      <td>510.208133</td>
      <td>350.0</td>
      <td>608.00</td>
      <td>853.0</td>
      <td>1105.00</td>
      <td>4391.0</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>201.0</td>
      <td>949.194030</td>
      <td>505.071586</td>
      <td>350.0</td>
      <td>609.00</td>
      <td>854.0</td>
      <td>1110.00</td>
      <td>4297.0</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>201.0</td>
      <td>950.751244</td>
      <td>512.245476</td>
      <td>350.0</td>
      <td>609.00</td>
      <td>854.0</td>
      <td>1114.00</td>
      <td>4502.0</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>201.0</td>
      <td>951.184080</td>
      <td>507.010139</td>
      <td>350.0</td>
      <td>609.00</td>
      <td>854.0</td>
      <td>1118.00</td>
      <td>4238.0</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>201.0</td>
      <td>952.328358</td>
      <td>508.250747</td>
      <td>350.0</td>
      <td>610.00</td>
      <td>854.0</td>
      <td>1122.00</td>
      <td>4270.0</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>201.0</td>
      <td>951.980100</td>
      <td>501.901006</td>
      <td>350.0</td>
      <td>610.00</td>
      <td>854.0</td>
      <td>1126.00</td>
      <td>3914.0</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>201.0</td>
      <td>949.084577</td>
      <td>484.808733</td>
      <td>350.0</td>
      <td>610.00</td>
      <td>854.0</td>
      <td>1131.00</td>
      <td>3483.0</td>
    </tr>
    <tr>
      <th>1809</th>
      <td>201.0</td>
      <td>950.144279</td>
      <td>486.675173</td>
      <td>350.0</td>
      <td>611.00</td>
      <td>855.0</td>
      <td>1135.00</td>
      <td>3430.0</td>
    </tr>
    <tr>
      <th>1810</th>
      <td>201.0</td>
      <td>954.069652</td>
      <td>503.353738</td>
      <td>350.0</td>
      <td>611.00</td>
      <td>855.0</td>
      <td>1139.00</td>
      <td>3927.0</td>
    </tr>
    <tr>
      <th>1811</th>
      <td>201.0</td>
      <td>954.900498</td>
      <td>502.759147</td>
      <td>350.0</td>
      <td>611.00</td>
      <td>855.0</td>
      <td>1143.00</td>
      <td>3966.0</td>
    </tr>
    <tr>
      <th>1812</th>
      <td>201.0</td>
      <td>951.721393</td>
      <td>483.557941</td>
      <td>351.0</td>
      <td>612.00</td>
      <td>855.0</td>
      <td>1148.00</td>
      <td>3447.0</td>
    </tr>
    <tr>
      <th>1813</th>
      <td>201.0</td>
      <td>951.910448</td>
      <td>480.106959</td>
      <td>351.0</td>
      <td>612.00</td>
      <td>855.0</td>
      <td>1152.00</td>
      <td>3423.0</td>
    </tr>
    <tr>
      <th>1814</th>
      <td>201.0</td>
      <td>951.890547</td>
      <td>475.997971</td>
      <td>351.0</td>
      <td>612.00</td>
      <td>855.0</td>
      <td>1156.00</td>
      <td>3296.0</td>
    </tr>
    <tr>
      <th>1815</th>
      <td>201.0</td>
      <td>958.572139</td>
      <td>506.941492</td>
      <td>351.0</td>
      <td>613.00</td>
      <td>856.0</td>
      <td>1160.00</td>
      <td>3945.0</td>
    </tr>
    <tr>
      <th>1816</th>
      <td>201.0</td>
      <td>956.601990</td>
      <td>493.924236</td>
      <td>351.0</td>
      <td>613.00</td>
      <td>856.0</td>
      <td>1162.00</td>
      <td>3748.0</td>
    </tr>
    <tr>
      <th>1817</th>
      <td>201.0</td>
      <td>957.452736</td>
      <td>495.306853</td>
      <td>351.0</td>
      <td>613.00</td>
      <td>856.0</td>
      <td>1163.00</td>
      <td>3778.0</td>
    </tr>
    <tr>
      <th>1818</th>
      <td>201.0</td>
      <td>959.199005</td>
      <td>498.796341</td>
      <td>351.0</td>
      <td>614.00</td>
      <td>856.0</td>
      <td>1164.00</td>
      <td>3831.0</td>
    </tr>
    <tr>
      <th>1819</th>
      <td>201.0</td>
      <td>958.338308</td>
      <td>491.285207</td>
      <td>351.0</td>
      <td>614.00</td>
      <td>857.0</td>
      <td>1166.00</td>
      <td>3645.0</td>
    </tr>
    <tr>
      <th>1820</th>
      <td>202.0</td>
      <td>963.356436</td>
      <td>503.232597</td>
      <td>351.0</td>
      <td>616.25</td>
      <td>859.0</td>
      <td>1167.75</td>
      <td>3900.0</td>
    </tr>
    <tr>
      <th>1821</th>
      <td>202.0</td>
      <td>969.821782</td>
      <td>506.892845</td>
      <td>351.0</td>
      <td>620.00</td>
      <td>865.0</td>
      <td>1172.25</td>
      <td>3815.0</td>
    </tr>
    <tr>
      <th>1822</th>
      <td>202.0</td>
      <td>973.980198</td>
      <td>509.388795</td>
      <td>351.0</td>
      <td>624.00</td>
      <td>873.5</td>
      <td>1175.25</td>
      <td>3843.0</td>
    </tr>
    <tr>
      <th>1823</th>
      <td>202.0</td>
      <td>979.663366</td>
      <td>517.761385</td>
      <td>351.0</td>
      <td>627.00</td>
      <td>880.0</td>
      <td>1178.75</td>
      <td>4028.0</td>
    </tr>
    <tr>
      <th>1824</th>
      <td>202.0</td>
      <td>985.866337</td>
      <td>524.615089</td>
      <td>351.0</td>
      <td>630.75</td>
      <td>885.5</td>
      <td>1183.75</td>
      <td>3992.0</td>
    </tr>
    <tr>
      <th>1825</th>
      <td>202.0</td>
      <td>990.945545</td>
      <td>525.364495</td>
      <td>351.0</td>
      <td>634.25</td>
      <td>891.5</td>
      <td>1192.50</td>
      <td>3883.0</td>
    </tr>
    <tr>
      <th>1826</th>
      <td>202.0</td>
      <td>995.668317</td>
      <td>525.688238</td>
      <td>351.0</td>
      <td>636.75</td>
      <td>893.0</td>
      <td>1198.75</td>
      <td>3937.0</td>
    </tr>
    <tr>
      <th>1827</th>
      <td>202.0</td>
      <td>1002.648515</td>
      <td>539.608399</td>
      <td>351.0</td>
      <td>640.00</td>
      <td>897.5</td>
      <td>1206.00</td>
      <td>4163.0</td>
    </tr>
    <tr>
      <th>1828</th>
      <td>202.0</td>
      <td>1007.316832</td>
      <td>542.955299</td>
      <td>351.0</td>
      <td>641.75</td>
      <td>899.5</td>
      <td>1212.50</td>
      <td>4245.0</td>
    </tr>
    <tr>
      <th>1829</th>
      <td>202.0</td>
      <td>1012.386139</td>
      <td>544.614346</td>
      <td>351.0</td>
      <td>644.00</td>
      <td>901.5</td>
      <td>1219.75</td>
      <td>4244.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1985</th>
      <td>202.0</td>
      <td>12104.945545</td>
      <td>15597.835363</td>
      <td>379.0</td>
      <td>2413.50</td>
      <td>6117.5</td>
      <td>16436.00</td>
      <td>129469.0</td>
    </tr>
    <tr>
      <th>1986</th>
      <td>202.0</td>
      <td>12013.420792</td>
      <td>14336.102099</td>
      <td>383.0</td>
      <td>2423.25</td>
      <td>6271.5</td>
      <td>17079.75</td>
      <td>100191.0</td>
    </tr>
    <tr>
      <th>1987</th>
      <td>202.0</td>
      <td>12212.856436</td>
      <td>14459.725539</td>
      <td>405.0</td>
      <td>2334.00</td>
      <td>6493.5</td>
      <td>17480.75</td>
      <td>101308.0</td>
    </tr>
    <tr>
      <th>1988</th>
      <td>202.0</td>
      <td>12351.866337</td>
      <td>14130.981128</td>
      <td>441.0</td>
      <td>2346.50</td>
      <td>6762.0</td>
      <td>17869.25</td>
      <td>82687.0</td>
    </tr>
    <tr>
      <th>1989</th>
      <td>202.0</td>
      <td>12640.628713</td>
      <td>14683.192281</td>
      <td>461.0</td>
      <td>2378.25</td>
      <td>7056.5</td>
      <td>19049.75</td>
      <td>92115.0</td>
    </tr>
    <tr>
      <th>1990</th>
      <td>203.0</td>
      <td>12814.029557</td>
      <td>15447.960817</td>
      <td>462.0</td>
      <td>2391.50</td>
      <td>7391.0</td>
      <td>17262.50</td>
      <td>114832.0</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>203.0</td>
      <td>12557.497537</td>
      <td>15231.577788</td>
      <td>439.0</td>
      <td>2394.50</td>
      <td>6841.0</td>
      <td>17365.50</td>
      <td>109658.0</td>
    </tr>
    <tr>
      <th>1992</th>
      <td>203.0</td>
      <td>12622.561576</td>
      <td>15661.156941</td>
      <td>290.0</td>
      <td>2276.50</td>
      <td>6833.0</td>
      <td>16371.00</td>
      <td>107416.0</td>
    </tr>
    <tr>
      <th>1993</th>
      <td>203.0</td>
      <td>12655.995074</td>
      <td>15898.350154</td>
      <td>197.0</td>
      <td>2194.00</td>
      <td>6424.0</td>
      <td>16161.50</td>
      <td>103224.0</td>
    </tr>
    <tr>
      <th>1994</th>
      <td>203.0</td>
      <td>12885.719212</td>
      <td>16288.687482</td>
      <td>153.0</td>
      <td>2176.00</td>
      <td>6310.0</td>
      <td>16239.50</td>
      <td>104855.0</td>
    </tr>
    <tr>
      <th>1995</th>
      <td>203.0</td>
      <td>13171.694581</td>
      <td>16668.405391</td>
      <td>142.0</td>
      <td>2206.00</td>
      <td>6353.0</td>
      <td>16957.50</td>
      <td>106425.0</td>
    </tr>
    <tr>
      <th>1996</th>
      <td>203.0</td>
      <td>13469.684729</td>
      <td>16860.883665</td>
      <td>151.0</td>
      <td>2295.00</td>
      <td>6536.0</td>
      <td>17601.00</td>
      <td>106923.0</td>
    </tr>
    <tr>
      <th>1997</th>
      <td>203.0</td>
      <td>13948.665025</td>
      <td>17590.191129</td>
      <td>289.0</td>
      <td>2388.50</td>
      <td>7036.0</td>
      <td>18188.00</td>
      <td>109553.0</td>
    </tr>
    <tr>
      <th>1998</th>
      <td>203.0</td>
      <td>14220.857143</td>
      <td>17797.886289</td>
      <td>346.0</td>
      <td>2422.00</td>
      <td>7310.0</td>
      <td>18422.00</td>
      <td>107276.0</td>
    </tr>
    <tr>
      <th>1999</th>
      <td>203.0</td>
      <td>14442.221675</td>
      <td>17962.485311</td>
      <td>397.0</td>
      <td>2516.50</td>
      <td>7528.0</td>
      <td>18842.00</td>
      <td>107741.0</td>
    </tr>
    <tr>
      <th>2000</th>
      <td>203.0</td>
      <td>14905.482759</td>
      <td>18630.515288</td>
      <td>473.0</td>
      <td>2599.00</td>
      <td>7695.0</td>
      <td>19202.50</td>
      <td>112238.0</td>
    </tr>
    <tr>
      <th>2001</th>
      <td>203.0</td>
      <td>15068.620690</td>
      <td>18633.198711</td>
      <td>506.0</td>
      <td>2646.00</td>
      <td>7903.0</td>
      <td>19191.50</td>
      <td>112539.0</td>
    </tr>
    <tr>
      <th>2002</th>
      <td>203.0</td>
      <td>15250.655172</td>
      <td>18807.803098</td>
      <td>507.0</td>
      <td>2661.00</td>
      <td>8013.0</td>
      <td>20113.50</td>
      <td>117133.0</td>
    </tr>
    <tr>
      <th>2003</th>
      <td>203.0</td>
      <td>15587.847291</td>
      <td>19160.769118</td>
      <td>474.0</td>
      <td>2773.00</td>
      <td>8162.0</td>
      <td>21398.50</td>
      <td>115622.0</td>
    </tr>
    <tr>
      <th>2004</th>
      <td>203.0</td>
      <td>16248.192118</td>
      <td>19952.627225</td>
      <td>441.0</td>
      <td>2842.50</td>
      <td>8651.0</td>
      <td>22572.00</td>
      <td>126335.0</td>
    </tr>
    <tr>
      <th>2005</th>
      <td>203.0</td>
      <td>16677.280788</td>
      <td>19942.838756</td>
      <td>470.0</td>
      <td>2975.00</td>
      <td>8764.0</td>
      <td>23713.00</td>
      <td>119134.0</td>
    </tr>
    <tr>
      <th>2006</th>
      <td>203.0</td>
      <td>17291.788177</td>
      <td>20490.662870</td>
      <td>499.0</td>
      <td>3168.50</td>
      <td>9568.0</td>
      <td>24788.50</td>
      <td>127563.0</td>
    </tr>
    <tr>
      <th>2007</th>
      <td>203.0</td>
      <td>17871.660099</td>
      <td>20714.120371</td>
      <td>555.0</td>
      <td>3280.00</td>
      <td>10233.0</td>
      <td>26037.00</td>
      <td>126364.0</td>
    </tr>
    <tr>
      <th>2008</th>
      <td>203.0</td>
      <td>17965.694581</td>
      <td>20334.512435</td>
      <td>588.0</td>
      <td>3367.00</td>
      <td>10425.0</td>
      <td>25239.50</td>
      <td>126076.0</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>203.0</td>
      <td>17202.374384</td>
      <td>19160.362441</td>
      <td>607.0</td>
      <td>3287.50</td>
      <td>10289.0</td>
      <td>23561.50</td>
      <td>122655.0</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>203.0</td>
      <td>17559.950739</td>
      <td>19685.759131</td>
      <td>614.0</td>
      <td>3394.00</td>
      <td>10515.0</td>
      <td>24702.00</td>
      <td>127984.0</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>204.0</td>
      <td>18019.333333</td>
      <td>20420.280357</td>
      <td>614.0</td>
      <td>3508.75</td>
      <td>11049.0</td>
      <td>25232.00</td>
      <td>133734.0</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>203.0</td>
      <td>18127.674877</td>
      <td>20504.649685</td>
      <td>616.0</td>
      <td>3675.00</td>
      <td>11046.0</td>
      <td>24876.00</td>
      <td>130990.0</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>203.0</td>
      <td>18305.502463</td>
      <td>20782.622473</td>
      <td>584.0</td>
      <td>3788.00</td>
      <td>11405.0</td>
      <td>25029.50</td>
      <td>136540.0</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>203.0</td>
      <td>18628.310345</td>
      <td>21262.409355</td>
      <td>578.0</td>
      <td>3796.50</td>
      <td>11514.0</td>
      <td>25786.50</td>
      <td>142893.0</td>
    </tr>
  </tbody>
</table>
<p>215 rows × 8 columns</p>
</div>



## 25


```python
by_year.mean()
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
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1800</th>
      <td>946.288557</td>
      <td>31.486020</td>
      <td>4.149630e+06</td>
      <td>5.292930e+09</td>
    </tr>
    <tr>
      <th>1801</th>
      <td>946.661692</td>
      <td>31.448905</td>
      <td>4.167524e+06</td>
      <td>5.319338e+09</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>949.452736</td>
      <td>31.463483</td>
      <td>4.185563e+06</td>
      <td>5.360029e+09</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>949.194030</td>
      <td>31.377413</td>
      <td>4.203777e+06</td>
      <td>5.385297e+09</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>950.751244</td>
      <td>31.446318</td>
      <td>4.222136e+06</td>
      <td>5.422209e+09</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>951.184080</td>
      <td>31.562537</td>
      <td>4.240635e+06</td>
      <td>5.453558e+09</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>952.328358</td>
      <td>31.615970</td>
      <td>4.259263e+06</td>
      <td>5.486458e+09</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>951.980100</td>
      <td>31.573134</td>
      <td>4.278008e+06</td>
      <td>5.524610e+09</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>949.084577</td>
      <td>31.376766</td>
      <td>4.296867e+06</td>
      <td>5.541086e+09</td>
    </tr>
    <tr>
      <th>1809</th>
      <td>950.144279</td>
      <td>31.310448</td>
      <td>4.315812e+06</td>
      <td>5.579419e+09</td>
    </tr>
    <tr>
      <th>1810</th>
      <td>954.069652</td>
      <td>31.521741</td>
      <td>4.334875e+06</td>
      <td>5.612397e+09</td>
    </tr>
    <tr>
      <th>1811</th>
      <td>954.900498</td>
      <td>31.481891</td>
      <td>4.354265e+06</td>
      <td>5.633909e+09</td>
    </tr>
    <tr>
      <th>1812</th>
      <td>951.721393</td>
      <td>31.472736</td>
      <td>4.373879e+06</td>
      <td>5.648213e+09</td>
    </tr>
    <tr>
      <th>1813</th>
      <td>951.910448</td>
      <td>31.467214</td>
      <td>4.393649e+06</td>
      <td>5.692809e+09</td>
    </tr>
    <tr>
      <th>1814</th>
      <td>951.890547</td>
      <td>31.516318</td>
      <td>4.413575e+06</td>
      <td>5.719493e+09</td>
    </tr>
    <tr>
      <th>1815</th>
      <td>958.572139</td>
      <td>31.647413</td>
      <td>4.433686e+06</td>
      <td>5.774900e+09</td>
    </tr>
    <tr>
      <th>1816</th>
      <td>956.601990</td>
      <td>31.627512</td>
      <td>4.453991e+06</td>
      <td>5.779540e+09</td>
    </tr>
    <tr>
      <th>1817</th>
      <td>957.452736</td>
      <td>31.721542</td>
      <td>4.474464e+06</td>
      <td>5.814422e+09</td>
    </tr>
    <tr>
      <th>1818</th>
      <td>959.199005</td>
      <td>31.574726</td>
      <td>4.495060e+06</td>
      <td>5.862469e+09</td>
    </tr>
    <tr>
      <th>1819</th>
      <td>958.338308</td>
      <td>31.488607</td>
      <td>4.515803e+06</td>
      <td>5.884003e+09</td>
    </tr>
    <tr>
      <th>1820</th>
      <td>963.356436</td>
      <td>31.560796</td>
      <td>4.536700e+06</td>
      <td>5.915726e+09</td>
    </tr>
    <tr>
      <th>1821</th>
      <td>969.821782</td>
      <td>31.620597</td>
      <td>4.568149e+06</td>
      <td>5.988010e+09</td>
    </tr>
    <tr>
      <th>1822</th>
      <td>973.980198</td>
      <td>31.722090</td>
      <td>4.599823e+06</td>
      <td>6.025950e+09</td>
    </tr>
    <tr>
      <th>1823</th>
      <td>979.663366</td>
      <td>31.770647</td>
      <td>4.631721e+06</td>
      <td>6.087423e+09</td>
    </tr>
    <tr>
      <th>1824</th>
      <td>985.866337</td>
      <td>31.709005</td>
      <td>4.663854e+06</td>
      <td>6.158582e+09</td>
    </tr>
    <tr>
      <th>1825</th>
      <td>990.945545</td>
      <td>31.666816</td>
      <td>4.696225e+06</td>
      <td>6.218656e+09</td>
    </tr>
    <tr>
      <th>1826</th>
      <td>995.668317</td>
      <td>31.597313</td>
      <td>4.728530e+06</td>
      <td>6.272059e+09</td>
    </tr>
    <tr>
      <th>1827</th>
      <td>1002.648515</td>
      <td>31.633582</td>
      <td>4.760875e+06</td>
      <td>6.347531e+09</td>
    </tr>
    <tr>
      <th>1828</th>
      <td>1007.316832</td>
      <td>31.577861</td>
      <td>4.793402e+06</td>
      <td>6.380584e+09</td>
    </tr>
    <tr>
      <th>1829</th>
      <td>1012.386139</td>
      <td>31.559950</td>
      <td>4.826018e+06</td>
      <td>6.448246e+09</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1985</th>
      <td>12104.945545</td>
      <td>65.131683</td>
      <td>2.126360e+07</td>
      <td>2.004337e+11</td>
    </tr>
    <tr>
      <th>1986</th>
      <td>12013.420792</td>
      <td>65.545792</td>
      <td>2.163641e+07</td>
      <td>2.068168e+11</td>
    </tr>
    <tr>
      <th>1987</th>
      <td>12212.856436</td>
      <td>65.868069</td>
      <td>2.201880e+07</td>
      <td>2.137740e+11</td>
    </tr>
    <tr>
      <th>1988</th>
      <td>12351.866337</td>
      <td>66.144406</td>
      <td>2.240565e+07</td>
      <td>2.218612e+11</td>
    </tr>
    <tr>
      <th>1989</th>
      <td>12640.628713</td>
      <td>66.402475</td>
      <td>2.278707e+07</td>
      <td>2.286743e+11</td>
    </tr>
    <tr>
      <th>1990</th>
      <td>12814.029557</td>
      <td>66.784615</td>
      <td>2.316234e+07</td>
      <td>2.321704e+11</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>12557.497537</td>
      <td>66.844663</td>
      <td>2.353319e+07</td>
      <td>2.344332e+11</td>
    </tr>
    <tr>
      <th>1992</th>
      <td>12622.561576</td>
      <td>67.026875</td>
      <td>2.389015e+07</td>
      <td>2.382744e+11</td>
    </tr>
    <tr>
      <th>1993</th>
      <td>12655.995074</td>
      <td>67.092500</td>
      <td>2.423275e+07</td>
      <td>2.425276e+11</td>
    </tr>
    <tr>
      <th>1994</th>
      <td>12885.719212</td>
      <td>67.006106</td>
      <td>2.456898e+07</td>
      <td>2.498521e+11</td>
    </tr>
    <tr>
      <th>1995</th>
      <td>13171.694581</td>
      <td>67.220000</td>
      <td>2.490143e+07</td>
      <td>2.581019e+11</td>
    </tr>
    <tr>
      <th>1996</th>
      <td>13469.684729</td>
      <td>67.412404</td>
      <td>2.522809e+07</td>
      <td>2.680382e+11</td>
    </tr>
    <tr>
      <th>1997</th>
      <td>13948.665025</td>
      <td>67.623541</td>
      <td>2.554911e+07</td>
      <td>2.788527e+11</td>
    </tr>
    <tr>
      <th>1998</th>
      <td>14220.857143</td>
      <td>67.762344</td>
      <td>2.586722e+07</td>
      <td>2.855597e+11</td>
    </tr>
    <tr>
      <th>1999</th>
      <td>14442.221675</td>
      <td>67.934880</td>
      <td>2.618334e+07</td>
      <td>2.956431e+11</td>
    </tr>
    <tr>
      <th>2000</th>
      <td>14905.482759</td>
      <td>68.077703</td>
      <td>2.650043e+07</td>
      <td>3.093815e+11</td>
    </tr>
    <tr>
      <th>2001</th>
      <td>15068.620690</td>
      <td>68.437943</td>
      <td>2.681894e+07</td>
      <td>3.167417e+11</td>
    </tr>
    <tr>
      <th>2002</th>
      <td>15250.655172</td>
      <td>68.653254</td>
      <td>2.713840e+07</td>
      <td>3.255249e+11</td>
    </tr>
    <tr>
      <th>2003</th>
      <td>15587.847291</td>
      <td>68.935550</td>
      <td>2.746062e+07</td>
      <td>3.375965e+11</td>
    </tr>
    <tr>
      <th>2004</th>
      <td>16248.192118</td>
      <td>69.184211</td>
      <td>2.778648e+07</td>
      <td>3.556785e+11</td>
    </tr>
    <tr>
      <th>2005</th>
      <td>16677.280788</td>
      <td>69.524019</td>
      <td>2.811636e+07</td>
      <td>3.724431e+11</td>
    </tr>
    <tr>
      <th>2006</th>
      <td>17291.788177</td>
      <td>69.850190</td>
      <td>2.845033e+07</td>
      <td>3.926470e+11</td>
    </tr>
    <tr>
      <th>2007</th>
      <td>17871.660099</td>
      <td>70.139712</td>
      <td>2.878812e+07</td>
      <td>4.140874e+11</td>
    </tr>
    <tr>
      <th>2008</th>
      <td>17965.694581</td>
      <td>70.447163</td>
      <td>2.912917e+07</td>
      <td>4.259501e+11</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>17202.374384</td>
      <td>70.767740</td>
      <td>2.912601e+07</td>
      <td>4.272031e+11</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>17559.950739</td>
      <td>70.969904</td>
      <td>2.948360e+07</td>
      <td>4.498648e+11</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>18019.333333</td>
      <td>71.324375</td>
      <td>3.048871e+07</td>
      <td>4.680519e+11</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>18127.674877</td>
      <td>71.663077</td>
      <td>3.085723e+07</td>
      <td>4.838351e+11</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>18305.502463</td>
      <td>71.916106</td>
      <td>3.122610e+07</td>
      <td>5.000853e+11</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>18628.310345</td>
      <td>72.088125</td>
      <td>3.159399e+07</td>
      <td>5.166226e+11</td>
    </tr>
  </tbody>
</table>
<p>215 rows × 4 columns</p>
</div>



## 26


```python
df['continent'].unique()
```




    array(['asia', 'americas', 'europe', 'africa'], dtype=object)



## 27


```python
df['continent'].nunique()
```




    4



## 28


```python
df['continent'].value_counts()
```




    asia        16304
    europe      14335
    africa      12679
    americas    11171
    Name: continent, dtype: int64



## 29


```python
asia_df = df[df['continent'] == 'asia']
asia_df
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2014</td>
      <td>asia</td>
      <td>Philippines</td>
      <td>6598.0</td>
      <td>70.70</td>
      <td>1.001022e+08</td>
      <td>6.604746e+11</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2014</td>
      <td>asia</td>
      <td>Palau</td>
      <td>14078.0</td>
      <td>NaN</td>
      <td>2.109400e+04</td>
      <td>2.969613e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2014</td>
      <td>asia</td>
      <td>Pakistan</td>
      <td>4619.0</td>
      <td>65.60</td>
      <td>1.855463e+08</td>
      <td>8.570382e+11</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2014</td>
      <td>asia</td>
      <td>Papua New Guinea</td>
      <td>2510.0</td>
      <td>60.50</td>
      <td>7.755785e+06</td>
      <td>1.946702e+10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2014</td>
      <td>asia</td>
      <td>Taiwan</td>
      <td>41376.0</td>
      <td>79.40</td>
      <td>2.318400e+07</td>
      <td>9.592612e+11</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2014</td>
      <td>asia</td>
      <td>New Zealand</td>
      <td>33538.0</td>
      <td>81.40</td>
      <td>4.566700e+06</td>
      <td>1.531580e+11</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2014</td>
      <td>asia</td>
      <td>Malaysia</td>
      <td>23579.0</td>
      <td>75.10</td>
      <td>3.022802e+07</td>
      <td>7.127464e+11</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2014</td>
      <td>asia</td>
      <td>Oman</td>
      <td>48201.0</td>
      <td>77.00</td>
      <td>3.960925e+06</td>
      <td>1.909205e+11</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2014</td>
      <td>asia</td>
      <td>Maldives</td>
      <td>14095.0</td>
      <td>80.00</td>
      <td>4.082470e+05</td>
      <td>5.754241e+09</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2014</td>
      <td>asia</td>
      <td>Macao, China</td>
      <td>142893.0</td>
      <td>80.61</td>
      <td>5.887810e+05</td>
      <td>8.413268e+10</td>
    </tr>
    <tr>
      <th>32</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kyrgyz Republic</td>
      <td>3169.0</td>
      <td>69.60</td>
      <td>5.774566e+06</td>
      <td>1.829960e+10</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kiribati</td>
      <td>1822.0</td>
      <td>62.80</td>
      <td>1.104580e+05</td>
      <td>2.012545e+08</td>
    </tr>
    <tr>
      <th>36</th>
      <td>2014</td>
      <td>asia</td>
      <td>American Samoa</td>
      <td>NaN</td>
      <td>72.80</td>
      <td>5.543700e+04</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>38</th>
      <td>2014</td>
      <td>asia</td>
      <td>Jordan</td>
      <td>11496.0</td>
      <td>78.40</td>
      <td>8.809306e+06</td>
      <td>1.012718e+11</td>
    </tr>
    <tr>
      <th>39</th>
      <td>2014</td>
      <td>asia</td>
      <td>Mongolia</td>
      <td>11509.0</td>
      <td>66.80</td>
      <td>2.923896e+06</td>
      <td>3.365112e+10</td>
    </tr>
    <tr>
      <th>41</th>
      <td>2014</td>
      <td>asia</td>
      <td>Israel</td>
      <td>31180.0</td>
      <td>81.30</td>
      <td>7.941329e+06</td>
      <td>2.476106e+11</td>
    </tr>
    <tr>
      <th>43</th>
      <td>2014</td>
      <td>asia</td>
      <td>Japan</td>
      <td>35635.0</td>
      <td>83.10</td>
      <td>1.281629e+08</td>
      <td>4.567084e+12</td>
    </tr>
    <tr>
      <th>45</th>
      <td>2014</td>
      <td>asia</td>
      <td>Iran</td>
      <td>15573.0</td>
      <td>74.60</td>
      <td>7.841109e+07</td>
      <td>1.221096e+12</td>
    </tr>
    <tr>
      <th>48</th>
      <td>2014</td>
      <td>asia</td>
      <td>India</td>
      <td>5565.0</td>
      <td>66.90</td>
      <td>1.293859e+09</td>
      <td>7.200327e+12</td>
    </tr>
    <tr>
      <th>49</th>
      <td>2014</td>
      <td>asia</td>
      <td>Tuvalu</td>
      <td>3548.0</td>
      <td>NaN</td>
      <td>1.090800e+04</td>
      <td>3.870158e+07</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2014</td>
      <td>asia</td>
      <td>Fiji</td>
      <td>7735.0</td>
      <td>65.70</td>
      <td>8.858060e+05</td>
      <td>6.851709e+09</td>
    </tr>
    <tr>
      <th>53</th>
      <td>2014</td>
      <td>asia</td>
      <td>Hong Kong, China</td>
      <td>52552.0</td>
      <td>83.56</td>
      <td>7.194563e+06</td>
      <td>3.780887e+11</td>
    </tr>
    <tr>
      <th>54</th>
      <td>2014</td>
      <td>asia</td>
      <td>Vanuatu</td>
      <td>2837.0</td>
      <td>64.70</td>
      <td>2.588500e+05</td>
      <td>7.343574e+08</td>
    </tr>
    <tr>
      <th>55</th>
      <td>2014</td>
      <td>asia</td>
      <td>Tajikistan</td>
      <td>2533.0</td>
      <td>71.90</td>
      <td>8.362745e+06</td>
      <td>2.118283e+10</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2014</td>
      <td>asia</td>
      <td>Micronesia, Fed. Sts.</td>
      <td>3475.0</td>
      <td>68.80</td>
      <td>1.040150e+05</td>
      <td>3.614521e+08</td>
    </tr>
    <tr>
      <th>70</th>
      <td>2014</td>
      <td>asia</td>
      <td>Lao</td>
      <td>4925.0</td>
      <td>66.60</td>
      <td>6.576397e+06</td>
      <td>3.238876e+10</td>
    </tr>
    <tr>
      <th>72</th>
      <td>2014</td>
      <td>asia</td>
      <td>Nepal</td>
      <td>2265.0</td>
      <td>70.20</td>
      <td>2.832324e+07</td>
      <td>6.415214e+10</td>
    </tr>
    <tr>
      <th>75</th>
      <td>2014</td>
      <td>asia</td>
      <td>Australia</td>
      <td>43219.0</td>
      <td>82.30</td>
      <td>2.347467e+07</td>
      <td>1.014552e+12</td>
    </tr>
    <tr>
      <th>77</th>
      <td>2014</td>
      <td>asia</td>
      <td>Kuwait</td>
      <td>83394.0</td>
      <td>80.20</td>
      <td>3.782450e+06</td>
      <td>3.154336e+11</td>
    </tr>
    <tr>
      <th>78</th>
      <td>2014</td>
      <td>asia</td>
      <td>Brunei</td>
      <td>72219.0</td>
      <td>77.10</td>
      <td>4.117040e+05</td>
      <td>2.973285e+10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>54400</th>
      <td>1800</td>
      <td>asia</td>
      <td>Fiji</td>
      <td>785.0</td>
      <td>26.10</td>
      <td>1.305330e+05</td>
      <td>1.024684e+08</td>
    </tr>
    <tr>
      <th>54404</th>
      <td>1800</td>
      <td>asia</td>
      <td>Bhutan</td>
      <td>629.0</td>
      <td>28.80</td>
      <td>8.998900e+04</td>
      <td>5.660308e+07</td>
    </tr>
    <tr>
      <th>54409</th>
      <td>1800</td>
      <td>asia</td>
      <td>Myanmar</td>
      <td>840.0</td>
      <td>30.80</td>
      <td>3.506000e+06</td>
      <td>2.945040e+09</td>
    </tr>
    <tr>
      <th>54413</th>
      <td>1800</td>
      <td>asia</td>
      <td>Maldives</td>
      <td>842.0</td>
      <td>32.65</td>
      <td>4.237800e+04</td>
      <td>3.568228e+07</td>
    </tr>
    <tr>
      <th>54416</th>
      <td>1800</td>
      <td>asia</td>
      <td>Qatar</td>
      <td>1097.0</td>
      <td>30.80</td>
      <td>1.409200e+04</td>
      <td>1.545892e+07</td>
    </tr>
    <tr>
      <th>54419</th>
      <td>1800</td>
      <td>asia</td>
      <td>Samoa</td>
      <td>1400.0</td>
      <td>25.40</td>
      <td>4.730000e+04</td>
      <td>6.622000e+07</td>
    </tr>
    <tr>
      <th>54422</th>
      <td>1800</td>
      <td>asia</td>
      <td>Saudi Arabia</td>
      <td>846.0</td>
      <td>32.10</td>
      <td>2.091000e+06</td>
      <td>1.768986e+09</td>
    </tr>
    <tr>
      <th>54423</th>
      <td>1800</td>
      <td>asia</td>
      <td>Niue</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.538000e+03</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54425</th>
      <td>1800</td>
      <td>asia</td>
      <td>Singapore</td>
      <td>1021.0</td>
      <td>29.10</td>
      <td>3.000000e+04</td>
      <td>3.063000e+07</td>
    </tr>
    <tr>
      <th>54427</th>
      <td>1800</td>
      <td>asia</td>
      <td>Solomon Islands</td>
      <td>363.0</td>
      <td>25.10</td>
      <td>5.699800e+04</td>
      <td>2.069027e+07</td>
    </tr>
    <tr>
      <th>54429</th>
      <td>1800</td>
      <td>asia</td>
      <td>South Korea</td>
      <td>576.0</td>
      <td>25.80</td>
      <td>9.395000e+06</td>
      <td>5.411520e+09</td>
    </tr>
    <tr>
      <th>54432</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tuvalu</td>
      <td>719.0</td>
      <td>NaN</td>
      <td>2.499000e+03</td>
      <td>1.796781e+06</td>
    </tr>
    <tr>
      <th>54433</th>
      <td>1800</td>
      <td>asia</td>
      <td>Yemen</td>
      <td>877.0</td>
      <td>23.39</td>
      <td>2.593000e+06</td>
      <td>2.274061e+09</td>
    </tr>
    <tr>
      <th>54438</th>
      <td>1800</td>
      <td>asia</td>
      <td>Syria</td>
      <td>1081.0</td>
      <td>31.10</td>
      <td>1.337000e+06</td>
      <td>1.445297e+09</td>
    </tr>
    <tr>
      <th>54439</th>
      <td>1800</td>
      <td>asia</td>
      <td>Taiwan</td>
      <td>996.0</td>
      <td>28.30</td>
      <td>2.000000e+06</td>
      <td>1.992000e+09</td>
    </tr>
    <tr>
      <th>54440</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tajikistan</td>
      <td>556.0</td>
      <td>24.24</td>
      <td>4.666290e+05</td>
      <td>2.594457e+08</td>
    </tr>
    <tr>
      <th>54442</th>
      <td>1800</td>
      <td>asia</td>
      <td>Thailand</td>
      <td>931.0</td>
      <td>30.40</td>
      <td>4.665000e+06</td>
      <td>4.343115e+09</td>
    </tr>
    <tr>
      <th>54443</th>
      <td>1800</td>
      <td>asia</td>
      <td>Timor-Leste</td>
      <td>521.0</td>
      <td>28.95</td>
      <td>1.372620e+05</td>
      <td>7.151350e+07</td>
    </tr>
    <tr>
      <th>54445</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tonga</td>
      <td>663.0</td>
      <td>28.20</td>
      <td>1.865800e+04</td>
      <td>1.237025e+07</td>
    </tr>
    <tr>
      <th>54449</th>
      <td>1800</td>
      <td>asia</td>
      <td>Turkmenistan</td>
      <td>943.0</td>
      <td>24.00</td>
      <td>3.672150e+05</td>
      <td>3.462837e+08</td>
    </tr>
    <tr>
      <th>54450</th>
      <td>1800</td>
      <td>asia</td>
      <td>Vietnam</td>
      <td>861.0</td>
      <td>32.00</td>
      <td>6.551000e+06</td>
      <td>5.640411e+09</td>
    </tr>
    <tr>
      <th>54457</th>
      <td>1800</td>
      <td>asia</td>
      <td>Uzbekistan</td>
      <td>502.0</td>
      <td>26.93</td>
      <td>1.919159e+06</td>
      <td>9.634178e+08</td>
    </tr>
    <tr>
      <th>54458</th>
      <td>1800</td>
      <td>asia</td>
      <td>Vanuatu</td>
      <td>585.0</td>
      <td>24.30</td>
      <td>2.779100e+04</td>
      <td>1.625774e+07</td>
    </tr>
    <tr>
      <th>54467</th>
      <td>1800</td>
      <td>asia</td>
      <td>North Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.782615e+06</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54469</th>
      <td>1800</td>
      <td>asia</td>
      <td>American Samoa</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8.170000e+03</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54477</th>
      <td>1800</td>
      <td>asia</td>
      <td>Norfolk Island</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.121000e+03</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54478</th>
      <td>1800</td>
      <td>asia</td>
      <td>Northern Mariana Islands</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.360000e+03</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54480</th>
      <td>1800</td>
      <td>asia</td>
      <td>South Yemen (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.519280e+05</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54486</th>
      <td>1800</td>
      <td>asia</td>
      <td>Tokelau</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.009000e+03</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>54487</th>
      <td>1800</td>
      <td>asia</td>
      <td>United Korea (former)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.374000e+07</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>16304 rows × 7 columns</p>
</div>



## 30


```python
asia_df.groupby(by='year').mean()
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
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
    <tr>
      <th>year</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1800</th>
      <td>853.183333</td>
      <td>29.224576</td>
      <td>8.571324e+06</td>
      <td>1.041695e+10</td>
    </tr>
    <tr>
      <th>1801</th>
      <td>853.716667</td>
      <td>29.224407</td>
      <td>8.613720e+06</td>
      <td>1.047078e+10</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>854.366667</td>
      <td>29.216780</td>
      <td>8.656434e+06</td>
      <td>1.052596e+10</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>854.883333</td>
      <td>29.199661</td>
      <td>8.699470e+06</td>
      <td>1.058055e+10</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>855.450000</td>
      <td>29.191017</td>
      <td>8.742830e+06</td>
      <td>1.063632e+10</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>855.983333</td>
      <td>29.223729</td>
      <td>8.786517e+06</td>
      <td>1.069205e+10</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>856.566667</td>
      <td>29.223559</td>
      <td>8.830532e+06</td>
      <td>1.074818e+10</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>857.033333</td>
      <td>29.223390</td>
      <td>8.874880e+06</td>
      <td>1.080458e+10</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>857.666667</td>
      <td>29.223220</td>
      <td>8.919563e+06</td>
      <td>1.085876e+10</td>
    </tr>
    <tr>
      <th>1809</th>
      <td>858.200000</td>
      <td>29.223051</td>
      <td>8.964583e+06</td>
      <td>1.091612e+10</td>
    </tr>
    <tr>
      <th>1810</th>
      <td>858.783333</td>
      <td>29.222881</td>
      <td>9.009943e+06</td>
      <td>1.097389e+10</td>
    </tr>
    <tr>
      <th>1811</th>
      <td>859.283333</td>
      <td>29.222712</td>
      <td>9.055647e+06</td>
      <td>1.103233e+10</td>
    </tr>
    <tr>
      <th>1812</th>
      <td>859.933333</td>
      <td>29.138814</td>
      <td>9.101696e+06</td>
      <td>1.109107e+10</td>
    </tr>
    <tr>
      <th>1813</th>
      <td>860.450000</td>
      <td>29.222542</td>
      <td>9.148094e+06</td>
      <td>1.115038e+10</td>
    </tr>
    <tr>
      <th>1814</th>
      <td>861.000000</td>
      <td>29.222373</td>
      <td>9.194844e+06</td>
      <td>1.120980e+10</td>
    </tr>
    <tr>
      <th>1815</th>
      <td>861.600000</td>
      <td>29.222203</td>
      <td>9.241949e+06</td>
      <td>1.127019e+10</td>
    </tr>
    <tr>
      <th>1816</th>
      <td>862.183333</td>
      <td>29.222034</td>
      <td>9.289411e+06</td>
      <td>1.133035e+10</td>
    </tr>
    <tr>
      <th>1817</th>
      <td>862.800000</td>
      <td>29.221864</td>
      <td>9.337233e+06</td>
      <td>1.138894e+10</td>
    </tr>
    <tr>
      <th>1818</th>
      <td>863.283333</td>
      <td>29.221695</td>
      <td>9.385419e+06</td>
      <td>1.144992e+10</td>
    </tr>
    <tr>
      <th>1819</th>
      <td>863.850000</td>
      <td>29.221525</td>
      <td>9.433972e+06</td>
      <td>1.151219e+10</td>
    </tr>
    <tr>
      <th>1820</th>
      <td>864.416667</td>
      <td>29.237966</td>
      <td>9.482894e+06</td>
      <td>1.157399e+10</td>
    </tr>
    <tr>
      <th>1821</th>
      <td>866.733333</td>
      <td>29.254407</td>
      <td>9.536035e+06</td>
      <td>1.164325e+10</td>
    </tr>
    <tr>
      <th>1822</th>
      <td>869.100000</td>
      <td>29.270847</td>
      <td>9.589539e+06</td>
      <td>1.171148e+10</td>
    </tr>
    <tr>
      <th>1823</th>
      <td>871.583333</td>
      <td>29.287288</td>
      <td>9.643423e+06</td>
      <td>1.178411e+10</td>
    </tr>
    <tr>
      <th>1824</th>
      <td>874.583333</td>
      <td>29.303729</td>
      <td>9.697701e+06</td>
      <td>1.185394e+10</td>
    </tr>
    <tr>
      <th>1825</th>
      <td>877.433333</td>
      <td>29.303390</td>
      <td>9.752312e+06</td>
      <td>1.192495e+10</td>
    </tr>
    <tr>
      <th>1826</th>
      <td>879.766667</td>
      <td>29.303220</td>
      <td>9.807230e+06</td>
      <td>1.199527e+10</td>
    </tr>
    <tr>
      <th>1827</th>
      <td>882.416667</td>
      <td>29.303051</td>
      <td>9.862525e+06</td>
      <td>1.206691e+10</td>
    </tr>
    <tr>
      <th>1828</th>
      <td>884.916667</td>
      <td>29.302881</td>
      <td>9.918186e+06</td>
      <td>1.213837e+10</td>
    </tr>
    <tr>
      <th>1829</th>
      <td>888.050000</td>
      <td>29.302712</td>
      <td>9.974242e+06</td>
      <td>1.221820e+10</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1985</th>
      <td>14237.400000</td>
      <td>65.201356</td>
      <td>3.875614e+07</td>
      <td>1.796932e+11</td>
    </tr>
    <tr>
      <th>1986</th>
      <td>13439.400000</td>
      <td>65.641356</td>
      <td>3.954964e+07</td>
      <td>1.856164e+11</td>
    </tr>
    <tr>
      <th>1987</th>
      <td>13666.150000</td>
      <td>66.062712</td>
      <td>4.036611e+07</td>
      <td>1.948115e+11</td>
    </tr>
    <tr>
      <th>1988</th>
      <td>13395.966667</td>
      <td>66.449153</td>
      <td>4.119197e+07</td>
      <td>2.039095e+11</td>
    </tr>
    <tr>
      <th>1989</th>
      <td>13651.000000</td>
      <td>66.845085</td>
      <td>4.200834e+07</td>
      <td>2.119344e+11</td>
    </tr>
    <tr>
      <th>1990</th>
      <td>14172.883333</td>
      <td>67.312581</td>
      <td>4.279876e+07</td>
      <td>2.249891e+11</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>13694.133333</td>
      <td>67.322581</td>
      <td>4.356045e+07</td>
      <td>2.334594e+11</td>
    </tr>
    <tr>
      <th>1992</th>
      <td>14483.416667</td>
      <td>67.830806</td>
      <td>4.429538e+07</td>
      <td>2.467831e+11</td>
    </tr>
    <tr>
      <th>1993</th>
      <td>14857.750000</td>
      <td>68.021452</td>
      <td>4.500637e+07</td>
      <td>2.589407e+11</td>
    </tr>
    <tr>
      <th>1994</th>
      <td>15169.100000</td>
      <td>68.186290</td>
      <td>4.569852e+07</td>
      <td>2.727995e+11</td>
    </tr>
    <tr>
      <th>1995</th>
      <td>15595.550000</td>
      <td>68.165645</td>
      <td>4.637686e+07</td>
      <td>2.886775e+11</td>
    </tr>
    <tr>
      <th>1996</th>
      <td>15855.716667</td>
      <td>68.382581</td>
      <td>4.703983e+07</td>
      <td>3.060134e+11</td>
    </tr>
    <tr>
      <th>1997</th>
      <td>16383.950000</td>
      <td>68.558065</td>
      <td>4.768677e+07</td>
      <td>3.203989e+11</td>
    </tr>
    <tr>
      <th>1998</th>
      <td>16313.050000</td>
      <td>68.885161</td>
      <td>4.832209e+07</td>
      <td>3.246166e+11</td>
    </tr>
    <tr>
      <th>1999</th>
      <td>16356.033333</td>
      <td>69.181935</td>
      <td>4.895194e+07</td>
      <td>3.389975e+11</td>
    </tr>
    <tr>
      <th>2000</th>
      <td>16863.883333</td>
      <td>69.357419</td>
      <td>4.958144e+07</td>
      <td>3.569249e+11</td>
    </tr>
    <tr>
      <th>2001</th>
      <td>16819.816667</td>
      <td>69.710161</td>
      <td>5.020986e+07</td>
      <td>3.695604e+11</td>
    </tr>
    <tr>
      <th>2002</th>
      <td>17065.950000</td>
      <td>69.936935</td>
      <td>5.083517e+07</td>
      <td>3.861794e+11</td>
    </tr>
    <tr>
      <th>2003</th>
      <td>17504.366667</td>
      <td>70.380968</td>
      <td>5.145843e+07</td>
      <td>4.077365e+11</td>
    </tr>
    <tr>
      <th>2004</th>
      <td>18426.966667</td>
      <td>70.534032</td>
      <td>5.208003e+07</td>
      <td>4.366552e+11</td>
    </tr>
    <tr>
      <th>2005</th>
      <td>18588.650000</td>
      <td>70.916774</td>
      <td>5.270006e+07</td>
      <td>4.659883e+11</td>
    </tr>
    <tr>
      <th>2006</th>
      <td>19169.633333</td>
      <td>71.159206</td>
      <td>5.331868e+07</td>
      <td>5.010440e+11</td>
    </tr>
    <tr>
      <th>2007</th>
      <td>19505.416667</td>
      <td>71.489839</td>
      <td>5.393601e+07</td>
      <td>5.420399e+11</td>
    </tr>
    <tr>
      <th>2008</th>
      <td>19498.250000</td>
      <td>71.691613</td>
      <td>5.455189e+07</td>
      <td>5.682074e+11</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>18902.500000</td>
      <td>71.950806</td>
      <td>5.688868e+07</td>
      <td>5.915543e+11</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>19705.300000</td>
      <td>72.327097</td>
      <td>5.751951e+07</td>
      <td>6.389456e+11</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>20518.316667</td>
      <td>72.521129</td>
      <td>6.067650e+07</td>
      <td>6.780930e+11</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>20952.116667</td>
      <td>72.676290</td>
      <td>6.132942e+07</td>
      <td>7.141230e+11</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>21357.650000</td>
      <td>72.913710</td>
      <td>6.197603e+07</td>
      <td>7.530471e+11</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>22030.183333</td>
      <td>73.038065</td>
      <td>6.261239e+07</td>
      <td>7.929439e+11</td>
    </tr>
  </tbody>
</table>
<p>215 rows × 4 columns</p>
</div>



## 31


```python
df.sort_values(by = 'life_exp', axis = 0, ascending = False).head(10) # axis = 0 생략 가능
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
      <th>year</th>
      <th>continent</th>
      <th>country</th>
      <th>income</th>
      <th>life_exp</th>
      <th>population</th>
      <th>gross_income</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>373</th>
      <td>2013</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>43735.0</td>
      <td>84.8</td>
      <td>80788.0</td>
      <td>3.533263e+09</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2014</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>44929.0</td>
      <td>84.8</td>
      <td>79223.0</td>
      <td>3.559410e+09</td>
    </tr>
    <tr>
      <th>959</th>
      <td>2010</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>38982.0</td>
      <td>84.7</td>
      <td>84449.0</td>
      <td>3.291991e+09</td>
    </tr>
    <tr>
      <th>602</th>
      <td>2012</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>41926.0</td>
      <td>84.7</td>
      <td>82431.0</td>
      <td>3.456002e+09</td>
    </tr>
    <tr>
      <th>724</th>
      <td>2011</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>41958.0</td>
      <td>84.7</td>
      <td>83751.0</td>
      <td>3.514024e+09</td>
    </tr>
    <tr>
      <th>1194</th>
      <td>2009</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>41735.0</td>
      <td>84.6</td>
      <td>84462.0</td>
      <td>3.525022e+09</td>
    </tr>
    <tr>
      <th>1478</th>
      <td>2008</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>41426.0</td>
      <td>84.6</td>
      <td>83861.0</td>
      <td>3.474026e+09</td>
    </tr>
    <tr>
      <th>1684</th>
      <td>2007</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>43442.0</td>
      <td>84.5</td>
      <td>82683.0</td>
      <td>3.591915e+09</td>
    </tr>
    <tr>
      <th>1941</th>
      <td>2006</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>42738.0</td>
      <td>84.4</td>
      <td>80991.0</td>
      <td>3.461393e+09</td>
    </tr>
    <tr>
      <th>2190</th>
      <td>2005</td>
      <td>europe</td>
      <td>Andorra</td>
      <td>39787.0</td>
      <td>84.3</td>
      <td>78867.0</td>
      <td>3.137881e+09</td>
    </tr>
  </tbody>
</table>
</div>



## 32


```python
asia_df[asia_df['year'] == 2014].loc[:, 'life_exp'].mean()
```




    73.03806451612904



## 33


```python
df1 = pd.DataFrame([[1,2,3,4], [5,6,7,8], [9,10,11]])
df1
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
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



## 34


```python
df1 = pd.DataFrame({'A': ['A0', 'A1', 'A2', 'A3'], 'B': ['B0', 'B1', 'B2', 'B3'],  
                    'C': ['C0', 'C1', 'C2', 'C3'], 'D': ['D0', 'D1', 'D2', 'D3']})
df1
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.DataFrame({'A': ['A4', 'A5', 'A6', 'A7'], 'B': ['B4', 'B5', 'B6', 'B7'],  
                    'C': ['C4', 'C5', 'C6', 'C7'], 'D': ['D4', 'D5', 'D6', 'D7']}, index = [4,5,6,7])
df2
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>A4</td>
      <td>B4</td>
      <td>C4</td>
      <td>D4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>A5</td>
      <td>B5</td>
      <td>C5</td>
      <td>D5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>A6</td>
      <td>B6</td>
      <td>C6</td>
      <td>D6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>A7</td>
      <td>B7</td>
      <td>C7</td>
      <td>D7</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3 = pd.DataFrame({'A': ['A8', 'A9', 'A10', 'A11'], 'B': ['B8', 'B9', 'B10', 'B11'],  
                    'C': ['C8', 'C9', 'C10', 'C11'], 'D': ['D8', 'D9', 'D10', 'D11']}, index = [8,9,10,11])
df3
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8</th>
      <td>A8</td>
      <td>B8</td>
      <td>C8</td>
      <td>D8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>A9</td>
      <td>B9</td>
      <td>C9</td>
      <td>D9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>A10</td>
      <td>B10</td>
      <td>C10</td>
      <td>D10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>A11</td>
      <td>B11</td>
      <td>C11</td>
      <td>D11</td>
    </tr>
  </tbody>
</table>
</div>



## 35


```python
pd.concat([df1,df2,df3])
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>A4</td>
      <td>B4</td>
      <td>C4</td>
      <td>D4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>A5</td>
      <td>B5</td>
      <td>C5</td>
      <td>D5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>A6</td>
      <td>B6</td>
      <td>C6</td>
      <td>D6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>A7</td>
      <td>B7</td>
      <td>C7</td>
      <td>D7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>A8</td>
      <td>B8</td>
      <td>C8</td>
      <td>D8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>A9</td>
      <td>B9</td>
      <td>C9</td>
      <td>D9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>A10</td>
      <td>B10</td>
      <td>C10</td>
      <td>D10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>A11</td>
      <td>B11</td>
      <td>C11</td>
      <td>D11</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.concat([df1,df2,df3], axis = 1)
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A4</td>
      <td>B4</td>
      <td>C4</td>
      <td>D4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A5</td>
      <td>B5</td>
      <td>C5</td>
      <td>D5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A6</td>
      <td>B6</td>
      <td>C6</td>
      <td>D6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A7</td>
      <td>B7</td>
      <td>C7</td>
      <td>D7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A8</td>
      <td>B8</td>
      <td>C8</td>
      <td>D8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A9</td>
      <td>B9</td>
      <td>C9</td>
      <td>D9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A10</td>
      <td>B10</td>
      <td>C10</td>
      <td>D10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>A11</td>
      <td>B11</td>
      <td>C11</td>
      <td>D11</td>
    </tr>
  </tbody>
</table>
</div>



## 36


```python
df4 = pd.DataFrame({'A': ['A0', 'A1', 'A2', 'A3'], 'B': ['B0', 'B1', 'B2', 'B3'],  
                    'C': ['C0', 'C1', 'C2', 'C3'], 'D': ['D0', 'D1', 'D2', 'D3']})
df4
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df5 = pd.DataFrame({'E': ['A0', 'A1', 'A2', 'A3'], 'F': ['B0', 'B1', 'B2', 'B3'],  
                    'G': ['C0', 'C1', 'C2', 'C3'], 'H': ['D0', 'D1', 'D2', 'D3']})
df5
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
      <th>E</th>
      <th>F</th>
      <th>G</th>
      <th>H</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df6 = pd.DataFrame({'I': ['A0', 'A1', 'A2', 'A3'], 'J': ['B0', 'B1', 'B2', 'B3'],  
                    'K': ['C0', 'C1', 'C2', 'C3'], 'L': ['D0', 'D1', 'D2', 'D3']})
df6
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
      <th>I</th>
      <th>J</th>
      <th>K</th>
      <th>L</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.concat([df4,df5,df6], axis=1)
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
      <th>G</th>
      <th>H</th>
      <th>I</th>
      <th>J</th>
      <th>K</th>
      <th>L</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>



## 37


```python
left = pd.DataFrame({'key': ['K0', 'K1', 'K2', 'K3'],
                     'A': ['A0', 'A1', 'A2', 'A3'],
                     'B': ['B0', 'B1', 'B2', 'B3']})
   
right = pd.DataFrame({'key': ['K0', 'K1', 'K2', 'K4'],
                      'C': ['C0', 'C1', 'C2', 'C3'],
                      'D': ['D0', 'D1', 'D2', 'D3']})   
```


```python
pd.merge(left, right, how = 'inner')
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
      <th>key</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>K0</td>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>K1</td>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>K2</td>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
  </tbody>
</table>
</div>



## 38


```python
pd.merge(left, right, how = 'outer')
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
      <th>key</th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>K0</td>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>K1</td>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>K2</td>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>K3</td>
      <td>A3</td>
      <td>B3</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>K4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>



## 39


```python
df.pivot_table(values = 'income', index = ['year', 'continent'])
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
      <th></th>
      <th>income</th>
    </tr>
    <tr>
      <th>year</th>
      <th>continent</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="4" valign="top">1800</th>
      <th>africa</th>
      <td>626.833333</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1023.900000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>853.183333</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1366.127660</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1801</th>
      <th>africa</th>
      <td>627.351852</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1025.525000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>853.716667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1365.063830</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1802</th>
      <th>africa</th>
      <td>627.925926</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1026.975000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>854.366667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1374.276596</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1803</th>
      <th>africa</th>
      <td>628.462963</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1026.700000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>854.883333</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1372.127660</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1804</th>
      <th>africa</th>
      <td>629.055556</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1027.275000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>855.450000</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1376.893617</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1805</th>
      <th>africa</th>
      <td>629.740741</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1029.025000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>855.983333</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1375.787234</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1806</th>
      <th>africa</th>
      <td>630.351852</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1030.650000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>856.566667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>1377.851064</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">1807</th>
      <th>africa</th>
      <td>631.000000</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>1031.875000</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">2007</th>
      <th>asia</th>
      <td>19505.416667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>29885.795918</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2008</th>
      <th>africa</th>
      <td>5277.870370</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>18050.125000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>19498.250000</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>30002.673469</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2009</th>
      <th>africa</th>
      <td>5177.685185</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>17267.075000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>18902.500000</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>28319.469388</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2010</th>
      <th>africa</th>
      <td>5297.203704</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>17321.150000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>19705.300000</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>28641.979592</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2011</th>
      <th>africa</th>
      <td>5078.833333</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>18076.341463</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>20518.316667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>29172.612245</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2012</th>
      <th>africa</th>
      <td>5385.870370</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>17700.425000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>20952.116667</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>29059.938776</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2013</th>
      <th>africa</th>
      <td>5393.962963</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>17867.925000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>21357.650000</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>29154.428571</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">2014</th>
      <th>africa</th>
      <td>5367.425926</td>
    </tr>
    <tr>
      <th>americas</th>
      <td>18010.750000</td>
    </tr>
    <tr>
      <th>asia</th>
      <td>22030.183333</td>
    </tr>
    <tr>
      <th>europe</th>
      <td>29580.918367</td>
    </tr>
  </tbody>
</table>
<p>860 rows × 1 columns</p>
</div>




```python
df.pivot_table(values = 'income', index = ['continent', 'year'])
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
      <th></th>
      <th>income</th>
    </tr>
    <tr>
      <th>continent</th>
      <th>year</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="30" valign="top">africa</th>
      <th>1800</th>
      <td>626.833333</td>
    </tr>
    <tr>
      <th>1801</th>
      <td>627.351852</td>
    </tr>
    <tr>
      <th>1802</th>
      <td>627.925926</td>
    </tr>
    <tr>
      <th>1803</th>
      <td>628.462963</td>
    </tr>
    <tr>
      <th>1804</th>
      <td>629.055556</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>629.740741</td>
    </tr>
    <tr>
      <th>1806</th>
      <td>630.351852</td>
    </tr>
    <tr>
      <th>1807</th>
      <td>631.000000</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>631.555556</td>
    </tr>
    <tr>
      <th>1809</th>
      <td>632.148148</td>
    </tr>
    <tr>
      <th>1810</th>
      <td>632.703704</td>
    </tr>
    <tr>
      <th>1811</th>
      <td>633.333333</td>
    </tr>
    <tr>
      <th>1812</th>
      <td>633.981481</td>
    </tr>
    <tr>
      <th>1813</th>
      <td>634.518519</td>
    </tr>
    <tr>
      <th>1814</th>
      <td>635.185185</td>
    </tr>
    <tr>
      <th>1815</th>
      <td>635.777778</td>
    </tr>
    <tr>
      <th>1816</th>
      <td>636.314815</td>
    </tr>
    <tr>
      <th>1817</th>
      <td>636.981481</td>
    </tr>
    <tr>
      <th>1818</th>
      <td>637.648148</td>
    </tr>
    <tr>
      <th>1819</th>
      <td>638.222222</td>
    </tr>
    <tr>
      <th>1820</th>
      <td>638.796296</td>
    </tr>
    <tr>
      <th>1821</th>
      <td>646.037037</td>
    </tr>
    <tr>
      <th>1822</th>
      <td>646.148148</td>
    </tr>
    <tr>
      <th>1823</th>
      <td>648.722222</td>
    </tr>
    <tr>
      <th>1824</th>
      <td>651.277778</td>
    </tr>
    <tr>
      <th>1825</th>
      <td>653.907407</td>
    </tr>
    <tr>
      <th>1826</th>
      <td>656.425926</td>
    </tr>
    <tr>
      <th>1827</th>
      <td>658.981481</td>
    </tr>
    <tr>
      <th>1828</th>
      <td>661.518519</td>
    </tr>
    <tr>
      <th>1829</th>
      <td>664.037037</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="30" valign="top">europe</th>
      <th>1985</th>
      <td>19345.083333</td>
    </tr>
    <tr>
      <th>1986</th>
      <td>19889.666667</td>
    </tr>
    <tr>
      <th>1987</th>
      <td>20258.104167</td>
    </tr>
    <tr>
      <th>1988</th>
      <td>20818.958333</td>
    </tr>
    <tr>
      <th>1989</th>
      <td>21306.750000</td>
    </tr>
    <tr>
      <th>1990</th>
      <td>21085.326531</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>20547.020408</td>
    </tr>
    <tr>
      <th>1992</th>
      <td>19826.346939</td>
    </tr>
    <tr>
      <th>1993</th>
      <td>19442.857143</td>
    </tr>
    <tr>
      <th>1994</th>
      <td>19798.897959</td>
    </tr>
    <tr>
      <th>1995</th>
      <td>20363.571429</td>
    </tr>
    <tr>
      <th>1996</th>
      <td>20954.918367</td>
    </tr>
    <tr>
      <th>1997</th>
      <td>21736.163265</td>
    </tr>
    <tr>
      <th>1998</th>
      <td>22532.000000</td>
    </tr>
    <tr>
      <th>1999</th>
      <td>23195.673469</td>
    </tr>
    <tr>
      <th>2000</th>
      <td>24160.653061</td>
    </tr>
    <tr>
      <th>2001</th>
      <td>24658.836735</td>
    </tr>
    <tr>
      <th>2002</th>
      <td>25074.346939</td>
    </tr>
    <tr>
      <th>2003</th>
      <td>25592.591837</td>
    </tr>
    <tr>
      <th>2004</th>
      <td>26522.571429</td>
    </tr>
    <tr>
      <th>2005</th>
      <td>27397.918367</td>
    </tr>
    <tr>
      <th>2006</th>
      <td>28581.122449</td>
    </tr>
    <tr>
      <th>2007</th>
      <td>29885.795918</td>
    </tr>
    <tr>
      <th>2008</th>
      <td>30002.673469</td>
    </tr>
    <tr>
      <th>2009</th>
      <td>28319.469388</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>28641.979592</td>
    </tr>
    <tr>
      <th>2011</th>
      <td>29172.612245</td>
    </tr>
    <tr>
      <th>2012</th>
      <td>29059.938776</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>29154.428571</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>29580.918367</td>
    </tr>
  </tbody>
</table>
<p>860 rows × 1 columns</p>
</div>
