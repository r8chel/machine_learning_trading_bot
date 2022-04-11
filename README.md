# Machine Learning Trading Bot

---
This Jupyter Notebook attempts to improve existing computer algorithmic trading systems to increase competitive advantage in the market. 

## This notebook includes these steps

* Establish a Baseline Performance

* Tune the Baseline Trading Algorithm

* Evaluate a New Machine Learning Classifier

* Create an Evaluation Report

---

The baseline trading model showed a slight advantage of the Strategy Returns over the Actual Returns<br>
!['SVM Model with a 3 Month DataOffset and 4/100 Short/Long Window']('Images/SVCreturns_4_100_3m.png')<br>


The Linear Regression model showed a more significant advantage of the Strategy Returns over the Actual Returns<br>

!['LinearRegression Model with a 3 Month DataOffset and 4/100 Short/Long Window']('Images/LR_3m_returns.png')<br>


Comparitive Classification Report Data 3 Month, 4/100 Short/Long Window<br>
!['Comparitive Classification Report Data']('Images/Classification_4_100_3m.png')<br>


---

We then changed the DataOffset from 3 to 1 months and changed the Short Window to 50 which causes the Strategy and Actual Returns to be nearly identical in the SVM model, apparently overfitting the model.<br>

!['SVM Model with a 1 Month DataOffset and 50/100 Short/Long Window']('Images/SVCreturns_50_100_1.png')<br>

The same change resulted in a significant advantage of the Strategy over the Actual Returns with the Linear Regression Model.<br>
!['LinearRegression Model with a 1 Month DataOffset and a 50/100 Short/Long Window']('Images/LR_1m_returns.png')<br>

Comparitive Classification Report Data 1 Month, 50/100 Short/Long Window<br>
!['Comparitive Classification Report Data']('Images/Classification_50_100_1m.png')<br>

---
### Technologies

import pandas as pd
import numpy as np
from pathlib import Path
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from pandas.tseries.offsets import DateOffset
from sklearn.metrics import classification_reporta
from sklearn.linear_model 

---
### Contributors
Rachel Bates

---
### License
Creative Commons