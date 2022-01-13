```python
import pandas as pd
```


```python
df = pd.read_csv('bach_stem_enroll_field_procent.csv', error_bad_lines=False, delimiter=';')
df.head()
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
      <td>2012</td>
      <td>European Union - 27 countries (from 2020)</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Total</td>
      <td>Total</td>
      <td>:</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2012</td>
      <td>European Union - 27 countries (from 2020)</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Total</td>
      <td>Males</td>
      <td>:</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2012</td>
      <td>European Union - 27 countries (from 2020)</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Total</td>
      <td>Females</td>
      <td>:</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2012</td>
      <td>European Union - 27 countries (from 2020)</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Generic programmes and qualifications</td>
      <td>Total</td>
      <td>:</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2012</td>
      <td>European Union - 27 countries (from 2020)</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Generic programmes and qualifications</td>
      <td>Males</td>
      <td>:</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.tail()
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
      <th>170347</th>
      <td>2019</td>
      <td>Bosnia and Herzegovina</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Services not elsewhere classified</td>
      <td>Males</td>
      <td>:</td>
      <td>d</td>
    </tr>
    <tr>
      <th>170348</th>
      <td>2019</td>
      <td>Bosnia and Herzegovina</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Services not elsewhere classified</td>
      <td>Females</td>
      <td>:</td>
      <td>d</td>
    </tr>
    <tr>
      <th>170349</th>
      <td>2019</td>
      <td>Bosnia and Herzegovina</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Unknown</td>
      <td>Total</td>
      <td>0.4</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>170350</th>
      <td>2019</td>
      <td>Bosnia and Herzegovina</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Unknown</td>
      <td>Males</td>
      <td>0.2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>170351</th>
      <td>2019</td>
      <td>Bosnia and Herzegovina</td>
      <td>Percentage</td>
      <td>Bachelor's or equivalent level</td>
      <td>Unknown</td>
      <td>Females</td>
      <td>0.2</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = df.dropna(axis=0, how='any')
```


```python
df2 = df2[['TIME', 'GEO', 'ISCEDF13', 'SEX', 'Value']]
df2.head()
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
      <th>SEX</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>27324</th>
      <td>2013</td>
      <td>France</td>
      <td>Education</td>
      <td>Total</td>
      <td>0.4</td>
    </tr>
    <tr>
      <th>27325</th>
      <td>2013</td>
      <td>France</td>
      <td>Education</td>
      <td>Males</td>
      <td>0.1</td>
    </tr>
    <tr>
      <th>27326</th>
      <td>2013</td>
      <td>France</td>
      <td>Education</td>
      <td>Females</td>
      <td>0.3</td>
    </tr>
    <tr>
      <th>27345</th>
      <td>2013</td>
      <td>France</td>
      <td>Inter-disciplinary programmes and qualificatio...</td>
      <td>Total</td>
      <td>0.6</td>
    </tr>
    <tr>
      <th>27346</th>
      <td>2013</td>
      <td>France</td>
      <td>Inter-disciplinary programmes and qualificatio...</td>
      <td>Males</td>
      <td>0.2</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.drop(df2.index[df2['SEX'] == 'Males'], inplace = True)
```


```python
df2.head()
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
      <th>SEX</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>27324</th>
      <td>2013</td>
      <td>France</td>
      <td>Education</td>
      <td>Total</td>
      <td>0.4</td>
    </tr>
    <tr>
      <th>27326</th>
      <td>2013</td>
      <td>France</td>
      <td>Education</td>
      <td>Females</td>
      <td>0.3</td>
    </tr>
    <tr>
      <th>27345</th>
      <td>2013</td>
      <td>France</td>
      <td>Inter-disciplinary programmes and qualificatio...</td>
      <td>Total</td>
      <td>0.6</td>
    </tr>
    <tr>
      <th>27347</th>
      <td>2013</td>
      <td>France</td>
      <td>Inter-disciplinary programmes and qualificatio...</td>
      <td>Females</td>
      <td>0.4</td>
    </tr>
    <tr>
      <th>27510</th>
      <td>2013</td>
      <td>France</td>
      <td>Natural sciences, mathematics and statistics</td>
      <td>Total</td>
      <td>:</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.to_csv('education.csv')
```


```python

```
