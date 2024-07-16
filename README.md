## Dataset:
[Predict Future Slaes](https://www.kaggle.com/c/competitive-data-science-predict-future-sales)<br>
[Store Item Demand Forecasting Challenge](https://www.kaggle.com/c/competitive-data-science-predict-future-sales/data)

#### Time period of dataset:
```
Min date from train set: 2013-01-01
Max date from train set: 2017-12-31
```

## Implementation:

**Libraries:**  `NumPy` `pandas` `tensorflow` `matplotlib` `sklearn` `seaborn`
## Data Exploration:
<img src="https://github.com/Pradnya1208/Time-series-forecasting-using-Deep-Learning/blob/main/output/overall%20daily%20sales.PNG?raw=true">
<img src="https://github.com/Pradnya1208/Time-series-forecasting-using-Deep-Learning/blob/main/output/item%20daily%20sales.PNG?raw=true">
<img src ="https://github.com/Pradnya1208/Time-series-forecasting-using-Deep-Learning/blob/main/output/store%20sales.PNG?raw=true">

## Model training, evaluation, and prediction:
### Multilayer Perceptron:
- Multilayer Perceptron model or MLP model, here our model will have input features equal to the window size.
- MLP models don't take the input as sequenced data, so for the model, it is just receiving inputs and don't treat them as sequenced data, that may be a problem since the model won't see the data with the sequence pattern that it has.

### CNN Model:
- For the CNN model we will use one convolutional hidden layer followed by a max pooling layer. The filter maps are then flattened before being interpreted by a Dense layer and outputting a prediction.
- The convolutional layer should be able to identify patterns between the timesteps.

### LSTM:
- Now the LSTM model actually sees the input data as a sequence, so it's able to learn patterns from sequenced data (assuming it exists) better than the other ones, especially patterns from long sequences.

### CNN-LSTM:
- CNN-LSTM is a hybrid model for univariate time series forecasting.

- The benefit of this model is that the model can support very long input sequences that can be read as blocks or subsequences by the CNN model, then pieced together by the LSTM model.

### Comapring Models:
<img src ="https://github.com/Pradnya1208/Time-series-forecasting-using-Deep-Learning/blob/main/output/compare%20models.PNG?raw=true">
<br>

| Model             | Train RMSE             | Validation RMSE                                                                |
| ----------------- | -----------------| ------------------------------------------------------------------ |
| MLP | 18.36|  18.50 |
| CNN | 18.62|  18.76 |
| LSTM | 19.98|  18.76 |
| CNN-LSTM| 19.20 |  19.17 |



