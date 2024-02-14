# Machine-learning-for-cryptocurrency-market-prediction
Introduction :
In this project, we aim to predict the daily status of the coins in the crypto currency markets such as bitcoin
and classify them into three possible categories namely bearish, bullish or neutral. The categories are
specified by the Stochastic RSI, which is a technical indicator used in trading analysis to determine
overbought and oversold conditions of an asset. The stochastic RSI is calculated by applying the stochastic
oscillator formula to the RSI values instead of the price values. This can help to smooth out the RSI and
provide a more accurate signal of whether a security is overbought or oversold. The stochastic RSI can
oscillate between 0 and 100, just like the regular RSI. A reading above 80 is considered overbought, while
a reading below 20 is considered oversold. We calculated the stochastic RSI using a 14-days period RSI.
Traders can use the stochastic RSI to identify bullish or bearish divergences. A bullish divergence occurs
when the price of a security makes a lower low, but the stochastic RSI makes a higher low. This can signal
a potential trend reversal to the upside. Conversely, a bearish divergence occurs when the price of a
security makes a higher high, but the stochastic RSI makes a lower high. This can signal a potential trend
reversal to the downside.
In our code, we first load historical Bitcoin price data and look at some statistical information about
variables with the heatmap. After that we add the Stochastic RSI values to the main Data Frame and find
the maximum and minimum values. Then We added a new column to the Data Frame called “market
trend” that assigns the appropriate label to each observation (bearish, bullish, or neutral) based on 20th
percentile of the sorted Stochastic RSI values. This categorical variable is the response in our analysis.
By using Artificial Intelligence and statistical learning methods we seek to find the best model that can
classify the value of the “market trend” variable in each day based on the rolling windows of price changes
of bitcoin over the past 14 days.
We decided to use 4 of the best classification models namely KNN, SVM, RNN and TabNet and compare
their results and performances together to find the best model.
If we can successfully show that the 14-days price change can be used as a strong predictor for the market
trend of a cryptocurrency like bitcoin, it can create multiple business opportunities such as trading or even
giving recommendations to other traders based on the predictions of the most accurate model. Brokers,
individual traders, and trading journals such as Bloomberg can be potential users of this analysis.
Exploratory Analysis
After defining the “market trend” variable, we look at the bar chart to see what the frequencies of each
class are.
As you can see, the Stochastic RSI identified most of the days as neutral and both bearish and bullish labels
got approximately the same frequency. These frequencies suggest that we might get a very good accuracy
in classifying neutral days not for the fitness of our model but because of the dominant frequency of
neutral label.
In the figure below you can see the box plot of price change variable for each class.
