```python
import pandas as pd
```


```python
url = 'https://raw.githubusercontent.com/wblakecannon/DataCamp/master/10-cleaning-data-in-python/_datasets/airquality.csv'
df = pd.read_csv(url)
# Dataset is now stored in a Pandas Dataframe
```


```python
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
      <th>Ozone</th>
      <th>Solar.R</th>
      <th>Wind</th>
      <th>Temp</th>
      <th>Month</th>
      <th>Day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>41.0</td>
      <td>190.0</td>
      <td>7.4</td>
      <td>67</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>36.0</td>
      <td>118.0</td>
      <td>8.0</td>
      <td>72</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>12.0</td>
      <td>149.0</td>
      <td>12.6</td>
      <td>74</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>18.0</td>
      <td>313.0</td>
      <td>11.5</td>
      <td>62</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>14.3</td>
      <td>56</td>
      <td>5</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
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
      <th>Ozone</th>
      <th>Solar.R</th>
      <th>Wind</th>
      <th>Temp</th>
      <th>Month</th>
      <th>Day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>41.0</td>
      <td>190.0</td>
      <td>7.4</td>
      <td>67</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>36.0</td>
      <td>118.0</td>
      <td>8.0</td>
      <td>72</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>12.0</td>
      <td>149.0</td>
      <td>12.6</td>
      <td>74</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>18.0</td>
      <td>313.0</td>
      <td>11.5</td>
      <td>62</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>14.3</td>
      <td>56</td>
      <td>5</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>28.0</td>
      <td>NaN</td>
      <td>14.9</td>
      <td>66</td>
      <td>5</td>
      <td>6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>23.0</td>
      <td>299.0</td>
      <td>8.6</td>
      <td>65</td>
      <td>5</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>19.0</td>
      <td>99.0</td>
      <td>13.8</td>
      <td>59</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8.0</td>
      <td>19.0</td>
      <td>20.1</td>
      <td>61</td>
      <td>5</td>
      <td>9</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>194.0</td>
      <td>8.6</td>
      <td>69</td>
      <td>5</td>
      <td>10</td>
    </tr>
    <tr>
      <th>10</th>
      <td>7.0</td>
      <td>NaN</td>
      <td>6.9</td>
      <td>74</td>
      <td>5</td>
      <td>11</td>
    </tr>
    <tr>
      <th>11</th>
      <td>16.0</td>
      <td>256.0</td>
      <td>9.7</td>
      <td>69</td>
      <td>5</td>
      <td>12</td>
    </tr>
    <tr>
      <th>12</th>
      <td>11.0</td>
      <td>290.0</td>
      <td>9.2</td>
      <td>66</td>
      <td>5</td>
      <td>13</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.0</td>
      <td>274.0</td>
      <td>10.9</td>
      <td>68</td>
      <td>5</td>
      <td>14</td>
    </tr>
    <tr>
      <th>14</th>
      <td>18.0</td>
      <td>65.0</td>
      <td>13.2</td>
      <td>58</td>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>15</th>
      <td>14.0</td>
      <td>334.0</td>
      <td>11.5</td>
      <td>64</td>
      <td>5</td>
      <td>16</td>
    </tr>
    <tr>
      <th>16</th>
      <td>34.0</td>
      <td>307.0</td>
      <td>12.0</td>
      <td>66</td>
      <td>5</td>
      <td>17</td>
    </tr>
    <tr>
      <th>17</th>
      <td>6.0</td>
      <td>78.0</td>
      <td>18.4</td>
      <td>57</td>
      <td>5</td>
      <td>18</td>
    </tr>
    <tr>
      <th>18</th>
      <td>30.0</td>
      <td>322.0</td>
      <td>11.5</td>
      <td>68</td>
      <td>5</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>11.0</td>
      <td>44.0</td>
      <td>9.7</td>
      <td>62</td>
      <td>5</td>
      <td>20</td>
    </tr>
    <tr>
      <th>20</th>
      <td>1.0</td>
      <td>8.0</td>
      <td>9.7</td>
      <td>59</td>
      <td>5</td>
      <td>21</td>
    </tr>
    <tr>
      <th>21</th>
      <td>11.0</td>
      <td>320.0</td>
      <td>16.6</td>
      <td>73</td>
      <td>5</td>
      <td>22</td>
    </tr>
    <tr>
      <th>22</th>
      <td>4.0</td>
      <td>25.0</td>
      <td>9.7</td>
      <td>61</td>
      <td>5</td>
      <td>23</td>
    </tr>
    <tr>
      <th>23</th>
      <td>32.0</td>
      <td>92.0</td>
      <td>12.0</td>
      <td>61</td>
      <td>5</td>
      <td>24</td>
    </tr>
    <tr>
      <th>24</th>
      <td>NaN</td>
      <td>66.0</td>
      <td>16.6</td>
      <td>57</td>
      <td>5</td>
      <td>25</td>
    </tr>
    <tr>
      <th>25</th>
      <td>NaN</td>
      <td>266.0</td>
      <td>14.9</td>
      <td>58</td>
      <td>5</td>
      <td>26</td>
    </tr>
    <tr>
      <th>26</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>8.0</td>
      <td>57</td>
      <td>5</td>
      <td>27</td>
    </tr>
    <tr>
      <th>27</th>
      <td>23.0</td>
      <td>13.0</td>
      <td>12.0</td>
      <td>67</td>
      <td>5</td>
      <td>28</td>
    </tr>
    <tr>
      <th>28</th>
      <td>45.0</td>
      <td>252.0</td>
      <td>14.9</td>
      <td>81</td>
      <td>5</td>
      <td>29</td>
    </tr>
    <tr>
      <th>29</th>
      <td>115.0</td>
      <td>223.0</td>
      <td>5.7</td>
      <td>79</td>
      <td>5</td>
      <td>30</td>
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
      <th>123</th>
      <td>96.0</td>
      <td>167.0</td>
      <td>6.9</td>
      <td>91</td>
      <td>9</td>
      <td>1</td>
    </tr>
    <tr>
      <th>124</th>
      <td>78.0</td>
      <td>197.0</td>
      <td>5.1</td>
      <td>92</td>
      <td>9</td>
      <td>2</td>
    </tr>
    <tr>
      <th>125</th>
      <td>73.0</td>
      <td>183.0</td>
      <td>2.8</td>
      <td>93</td>
      <td>9</td>
      <td>3</td>
    </tr>
    <tr>
      <th>126</th>
      <td>91.0</td>
      <td>189.0</td>
      <td>4.6</td>
      <td>93</td>
      <td>9</td>
      <td>4</td>
    </tr>
    <tr>
      <th>127</th>
      <td>47.0</td>
      <td>95.0</td>
      <td>7.4</td>
      <td>87</td>
      <td>9</td>
      <td>5</td>
    </tr>
    <tr>
      <th>128</th>
      <td>32.0</td>
      <td>92.0</td>
      <td>15.5</td>
      <td>84</td>
      <td>9</td>
      <td>6</td>
    </tr>
    <tr>
      <th>129</th>
      <td>20.0</td>
      <td>252.0</td>
      <td>10.9</td>
      <td>80</td>
      <td>9</td>
      <td>7</td>
    </tr>
    <tr>
      <th>130</th>
      <td>23.0</td>
      <td>220.0</td>
      <td>10.3</td>
      <td>78</td>
      <td>9</td>
      <td>8</td>
    </tr>
    <tr>
      <th>131</th>
      <td>21.0</td>
      <td>230.0</td>
      <td>10.9</td>
      <td>75</td>
      <td>9</td>
      <td>9</td>
    </tr>
    <tr>
      <th>132</th>
      <td>24.0</td>
      <td>259.0</td>
      <td>9.7</td>
      <td>73</td>
      <td>9</td>
      <td>10</td>
    </tr>
    <tr>
      <th>133</th>
      <td>44.0</td>
      <td>236.0</td>
      <td>14.9</td>
      <td>81</td>
      <td>9</td>
      <td>11</td>
    </tr>
    <tr>
      <th>134</th>
      <td>21.0</td>
      <td>259.0</td>
      <td>15.5</td>
      <td>76</td>
      <td>9</td>
      <td>12</td>
    </tr>
    <tr>
      <th>135</th>
      <td>28.0</td>
      <td>238.0</td>
      <td>6.3</td>
      <td>77</td>
      <td>9</td>
      <td>13</td>
    </tr>
    <tr>
      <th>136</th>
      <td>9.0</td>
      <td>24.0</td>
      <td>10.9</td>
      <td>71</td>
      <td>9</td>
      <td>14</td>
    </tr>
    <tr>
      <th>137</th>
      <td>13.0</td>
      <td>112.0</td>
      <td>11.5</td>
      <td>71</td>
      <td>9</td>
      <td>15</td>
    </tr>
    <tr>
      <th>138</th>
      <td>46.0</td>
      <td>237.0</td>
      <td>6.9</td>
      <td>78</td>
      <td>9</td>
      <td>16</td>
    </tr>
    <tr>
      <th>139</th>
      <td>18.0</td>
      <td>224.0</td>
      <td>13.8</td>
      <td>67</td>
      <td>9</td>
      <td>17</td>
    </tr>
    <tr>
      <th>140</th>
      <td>13.0</td>
      <td>27.0</td>
      <td>10.3</td>
      <td>76</td>
      <td>9</td>
      <td>18</td>
    </tr>
    <tr>
      <th>141</th>
      <td>24.0</td>
      <td>238.0</td>
      <td>10.3</td>
      <td>68</td>
      <td>9</td>
      <td>19</td>
    </tr>
    <tr>
      <th>142</th>
      <td>16.0</td>
      <td>201.0</td>
      <td>8.0</td>
      <td>82</td>
      <td>9</td>
      <td>20</td>
    </tr>
    <tr>
      <th>143</th>
      <td>13.0</td>
      <td>238.0</td>
      <td>12.6</td>
      <td>64</td>
      <td>9</td>
      <td>21</td>
    </tr>
    <tr>
      <th>144</th>
      <td>23.0</td>
      <td>14.0</td>
      <td>9.2</td>
      <td>71</td>
      <td>9</td>
      <td>22</td>
    </tr>
    <tr>
      <th>145</th>
      <td>36.0</td>
      <td>139.0</td>
      <td>10.3</td>
      <td>81</td>
      <td>9</td>
      <td>23</td>
    </tr>
    <tr>
      <th>146</th>
      <td>7.0</td>
      <td>49.0</td>
      <td>10.3</td>
      <td>69</td>
      <td>9</td>
      <td>24</td>
    </tr>
    <tr>
      <th>147</th>
      <td>14.0</td>
      <td>20.0</td>
      <td>16.6</td>
      <td>63</td>
      <td>9</td>
      <td>25</td>
    </tr>
    <tr>
      <th>148</th>
      <td>30.0</td>
      <td>193.0</td>
      <td>6.9</td>
      <td>70</td>
      <td>9</td>
      <td>26</td>
    </tr>
    <tr>
      <th>149</th>
      <td>NaN</td>
      <td>145.0</td>
      <td>13.2</td>
      <td>77</td>
      <td>9</td>
      <td>27</td>
    </tr>
    <tr>
      <th>150</th>
      <td>14.0</td>
      <td>191.0</td>
      <td>14.3</td>
      <td>75</td>
      <td>9</td>
      <td>28</td>
    </tr>
    <tr>
      <th>151</th>
      <td>18.0</td>
      <td>131.0</td>
      <td>8.0</td>
      <td>76</td>
      <td>9</td>
      <td>29</td>
    </tr>
    <tr>
      <th>152</th>
      <td>20.0</td>
      <td>223.0</td>
      <td>11.5</td>
      <td>68</td>
      <td>9</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
<p>153 rows × 6 columns</p>
</div>




```python
#Imputation fills in the missing value with mean value for each column.
```


```python
df.fillna(df.mean(), inplace=True)
```


```python
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
      <th>Ozone</th>
      <th>Solar.R</th>
      <th>Wind</th>
      <th>Temp</th>
      <th>Month</th>
      <th>Day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>41.00000</td>
      <td>190.000000</td>
      <td>7.4</td>
      <td>67</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>36.00000</td>
      <td>118.000000</td>
      <td>8.0</td>
      <td>72</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>12.00000</td>
      <td>149.000000</td>
      <td>12.6</td>
      <td>74</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>18.00000</td>
      <td>313.000000</td>
      <td>11.5</td>
      <td>62</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>42.12931</td>
      <td>185.931507</td>
      <td>14.3</td>
      <td>56</td>
      <td>5</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>28.00000</td>
      <td>185.931507</td>
      <td>14.9</td>
      <td>66</td>
      <td>5</td>
      <td>6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>23.00000</td>
      <td>299.000000</td>
      <td>8.6</td>
      <td>65</td>
      <td>5</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>19.00000</td>
      <td>99.000000</td>
      <td>13.8</td>
      <td>59</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8.00000</td>
      <td>19.000000</td>
      <td>20.1</td>
      <td>61</td>
      <td>5</td>
      <td>9</td>
    </tr>
    <tr>
      <th>9</th>
      <td>42.12931</td>
      <td>194.000000</td>
      <td>8.6</td>
      <td>69</td>
      <td>5</td>
      <td>10</td>
    </tr>
    <tr>
      <th>10</th>
      <td>7.00000</td>
      <td>185.931507</td>
      <td>6.9</td>
      <td>74</td>
      <td>5</td>
      <td>11</td>
    </tr>
    <tr>
      <th>11</th>
      <td>16.00000</td>
      <td>256.000000</td>
      <td>9.7</td>
      <td>69</td>
      <td>5</td>
      <td>12</td>
    </tr>
    <tr>
      <th>12</th>
      <td>11.00000</td>
      <td>290.000000</td>
      <td>9.2</td>
      <td>66</td>
      <td>5</td>
      <td>13</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14.00000</td>
      <td>274.000000</td>
      <td>10.9</td>
      <td>68</td>
      <td>5</td>
      <td>14</td>
    </tr>
    <tr>
      <th>14</th>
      <td>18.00000</td>
      <td>65.000000</td>
      <td>13.2</td>
      <td>58</td>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>15</th>
      <td>14.00000</td>
      <td>334.000000</td>
      <td>11.5</td>
      <td>64</td>
      <td>5</td>
      <td>16</td>
    </tr>
    <tr>
      <th>16</th>
      <td>34.00000</td>
      <td>307.000000</td>
      <td>12.0</td>
      <td>66</td>
      <td>5</td>
      <td>17</td>
    </tr>
    <tr>
      <th>17</th>
      <td>6.00000</td>
      <td>78.000000</td>
      <td>18.4</td>
      <td>57</td>
      <td>5</td>
      <td>18</td>
    </tr>
    <tr>
      <th>18</th>
      <td>30.00000</td>
      <td>322.000000</td>
      <td>11.5</td>
      <td>68</td>
      <td>5</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>11.00000</td>
      <td>44.000000</td>
      <td>9.7</td>
      <td>62</td>
      <td>5</td>
      <td>20</td>
    </tr>
    <tr>
      <th>20</th>
      <td>1.00000</td>
      <td>8.000000</td>
      <td>9.7</td>
      <td>59</td>
      <td>5</td>
      <td>21</td>
    </tr>
    <tr>
      <th>21</th>
      <td>11.00000</td>
      <td>320.000000</td>
      <td>16.6</td>
      <td>73</td>
      <td>5</td>
      <td>22</td>
    </tr>
    <tr>
      <th>22</th>
      <td>4.00000</td>
      <td>25.000000</td>
      <td>9.7</td>
      <td>61</td>
      <td>5</td>
      <td>23</td>
    </tr>
    <tr>
      <th>23</th>
      <td>32.00000</td>
      <td>92.000000</td>
      <td>12.0</td>
      <td>61</td>
      <td>5</td>
      <td>24</td>
    </tr>
    <tr>
      <th>24</th>
      <td>42.12931</td>
      <td>66.000000</td>
      <td>16.6</td>
      <td>57</td>
      <td>5</td>
      <td>25</td>
    </tr>
    <tr>
      <th>25</th>
      <td>42.12931</td>
      <td>266.000000</td>
      <td>14.9</td>
      <td>58</td>
      <td>5</td>
      <td>26</td>
    </tr>
    <tr>
      <th>26</th>
      <td>42.12931</td>
      <td>185.931507</td>
      <td>8.0</td>
      <td>57</td>
      <td>5</td>
      <td>27</td>
    </tr>
    <tr>
      <th>27</th>
      <td>23.00000</td>
      <td>13.000000</td>
      <td>12.0</td>
      <td>67</td>
      <td>5</td>
      <td>28</td>
    </tr>
    <tr>
      <th>28</th>
      <td>45.00000</td>
      <td>252.000000</td>
      <td>14.9</td>
      <td>81</td>
      <td>5</td>
      <td>29</td>
    </tr>
    <tr>
      <th>29</th>
      <td>115.00000</td>
      <td>223.000000</td>
      <td>5.7</td>
      <td>79</td>
      <td>5</td>
      <td>30</td>
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
      <th>123</th>
      <td>96.00000</td>
      <td>167.000000</td>
      <td>6.9</td>
      <td>91</td>
      <td>9</td>
      <td>1</td>
    </tr>
    <tr>
      <th>124</th>
      <td>78.00000</td>
      <td>197.000000</td>
      <td>5.1</td>
      <td>92</td>
      <td>9</td>
      <td>2</td>
    </tr>
    <tr>
      <th>125</th>
      <td>73.00000</td>
      <td>183.000000</td>
      <td>2.8</td>
      <td>93</td>
      <td>9</td>
      <td>3</td>
    </tr>
    <tr>
      <th>126</th>
      <td>91.00000</td>
      <td>189.000000</td>
      <td>4.6</td>
      <td>93</td>
      <td>9</td>
      <td>4</td>
    </tr>
    <tr>
      <th>127</th>
      <td>47.00000</td>
      <td>95.000000</td>
      <td>7.4</td>
      <td>87</td>
      <td>9</td>
      <td>5</td>
    </tr>
    <tr>
      <th>128</th>
      <td>32.00000</td>
      <td>92.000000</td>
      <td>15.5</td>
      <td>84</td>
      <td>9</td>
      <td>6</td>
    </tr>
    <tr>
      <th>129</th>
      <td>20.00000</td>
      <td>252.000000</td>
      <td>10.9</td>
      <td>80</td>
      <td>9</td>
      <td>7</td>
    </tr>
    <tr>
      <th>130</th>
      <td>23.00000</td>
      <td>220.000000</td>
      <td>10.3</td>
      <td>78</td>
      <td>9</td>
      <td>8</td>
    </tr>
    <tr>
      <th>131</th>
      <td>21.00000</td>
      <td>230.000000</td>
      <td>10.9</td>
      <td>75</td>
      <td>9</td>
      <td>9</td>
    </tr>
    <tr>
      <th>132</th>
      <td>24.00000</td>
      <td>259.000000</td>
      <td>9.7</td>
      <td>73</td>
      <td>9</td>
      <td>10</td>
    </tr>
    <tr>
      <th>133</th>
      <td>44.00000</td>
      <td>236.000000</td>
      <td>14.9</td>
      <td>81</td>
      <td>9</td>
      <td>11</td>
    </tr>
    <tr>
      <th>134</th>
      <td>21.00000</td>
      <td>259.000000</td>
      <td>15.5</td>
      <td>76</td>
      <td>9</td>
      <td>12</td>
    </tr>
    <tr>
      <th>135</th>
      <td>28.00000</td>
      <td>238.000000</td>
      <td>6.3</td>
      <td>77</td>
      <td>9</td>
      <td>13</td>
    </tr>
    <tr>
      <th>136</th>
      <td>9.00000</td>
      <td>24.000000</td>
      <td>10.9</td>
      <td>71</td>
      <td>9</td>
      <td>14</td>
    </tr>
    <tr>
      <th>137</th>
      <td>13.00000</td>
      <td>112.000000</td>
      <td>11.5</td>
      <td>71</td>
      <td>9</td>
      <td>15</td>
    </tr>
    <tr>
      <th>138</th>
      <td>46.00000</td>
      <td>237.000000</td>
      <td>6.9</td>
      <td>78</td>
      <td>9</td>
      <td>16</td>
    </tr>
    <tr>
      <th>139</th>
      <td>18.00000</td>
      <td>224.000000</td>
      <td>13.8</td>
      <td>67</td>
      <td>9</td>
      <td>17</td>
    </tr>
    <tr>
      <th>140</th>
      <td>13.00000</td>
      <td>27.000000</td>
      <td>10.3</td>
      <td>76</td>
      <td>9</td>
      <td>18</td>
    </tr>
    <tr>
      <th>141</th>
      <td>24.00000</td>
      <td>238.000000</td>
      <td>10.3</td>
      <td>68</td>
      <td>9</td>
      <td>19</td>
    </tr>
    <tr>
      <th>142</th>
      <td>16.00000</td>
      <td>201.000000</td>
      <td>8.0</td>
      <td>82</td>
      <td>9</td>
      <td>20</td>
    </tr>
    <tr>
      <th>143</th>
      <td>13.00000</td>
      <td>238.000000</td>
      <td>12.6</td>
      <td>64</td>
      <td>9</td>
      <td>21</td>
    </tr>
    <tr>
      <th>144</th>
      <td>23.00000</td>
      <td>14.000000</td>
      <td>9.2</td>
      <td>71</td>
      <td>9</td>
      <td>22</td>
    </tr>
    <tr>
      <th>145</th>
      <td>36.00000</td>
      <td>139.000000</td>
      <td>10.3</td>
      <td>81</td>
      <td>9</td>
      <td>23</td>
    </tr>
    <tr>
      <th>146</th>
      <td>7.00000</td>
      <td>49.000000</td>
      <td>10.3</td>
      <td>69</td>
      <td>9</td>
      <td>24</td>
    </tr>
    <tr>
      <th>147</th>
      <td>14.00000</td>
      <td>20.000000</td>
      <td>16.6</td>
      <td>63</td>
      <td>9</td>
      <td>25</td>
    </tr>
    <tr>
      <th>148</th>
      <td>30.00000</td>
      <td>193.000000</td>
      <td>6.9</td>
      <td>70</td>
      <td>9</td>
      <td>26</td>
    </tr>
    <tr>
      <th>149</th>
      <td>42.12931</td>
      <td>145.000000</td>
      <td>13.2</td>
      <td>77</td>
      <td>9</td>
      <td>27</td>
    </tr>
    <tr>
      <th>150</th>
      <td>14.00000</td>
      <td>191.000000</td>
      <td>14.3</td>
      <td>75</td>
      <td>9</td>
      <td>28</td>
    </tr>
    <tr>
      <th>151</th>
      <td>18.00000</td>
      <td>131.000000</td>
      <td>8.0</td>
      <td>76</td>
      <td>9</td>
      <td>29</td>
    </tr>
    <tr>
      <th>152</th>
      <td>20.00000</td>
      <td>223.000000</td>
      <td>11.5</td>
      <td>68</td>
      <td>9</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
<p>153 rows × 6 columns</p>
</div>




```python
# count the number of NaN values in each column - All values have been imputed!
print(df.isnull().sum())
```

    Ozone      0
    Solar.R    0
    Wind       0
    Temp       0
    Month      0
    Day        0
    dtype: int64
