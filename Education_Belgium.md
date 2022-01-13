```python
import pandas as pd
```


```python
df = pd.read_csv('participation_by_s_e.csv', delimiter=';')
```


```python
df.head(5)
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
      <th>TIME</th>
      <th>GEO</th>
      <th>UNIT</th>
      <th>ISCED11</th>
      <th>ISCEDF13</th>
      <th>SEX</th>
      <th>Value</th>
      <th>Flag and Footnotes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Business, administration and law</td>
      <td>Females</td>
      <td>10</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Law</td>
      <td>Females</td>
      <td>2,2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Natural sciences, mathematics and statistics</td>
      <td>Females</td>
      <td>0,7</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Information and Communication Technologies</td>
      <td>Females</td>
      <td>0,4</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Engineering, manufacturing and construction</td>
      <td>Females</td>
      <td>1,7</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df = df[['TIME','GEO','ISCEDF13','Value']]
```


```python
df.head(5)
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
      <th>TIME</th>
      <th>GEO</th>
      <th>ISCEDF13</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Business, administration and law</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Law</td>
      <td>2,2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Natural sciences, mathematics and statistics</td>
      <td>0,7</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Information and Communication Technologies</td>
      <td>0,4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2013</td>
      <td>Belgium</td>
      <td>Engineering, manufacturing and construction</td>
      <td>1,7</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.to_csv('educationbelgium.csv')
```


```python

```
