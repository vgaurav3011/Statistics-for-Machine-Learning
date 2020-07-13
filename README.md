# Statistics for Machine Learning

![Python 3.6](https://img.shields.io/badge/Python-3.6-brightgreen.svg)

> "By Statistics, we mean methods specially adopted to the elucidation of quantitative data affected to a marked extent by multiplicity of causes”.
                                                                            --Yule and Kendal

It is different from Business Analytics that can be defined as:
> “Business Analytics (BA) can be defined as the broad use of data and quantitative analysis for decision making within
organizations”.
-- Thomas Davenport

Statistics is broadly divided into two categories:
1. Descriptive
2. Inferential

**Descriptive Statistics** involves describing the data, summarising information from the data, and providing a convenient overview to the data in a brief. It is like online dating: it is definite but can be misleading.

For example, if we try to answer the question who is the best batsman in the world of all time in cricket, then there can be many factors to determine this which leads to a confusion. Descriptive statistics based approach may involve say taking the average of all the scores by a batsman and providing it as a single convenient value to evaluate the performance of batsman. This helps in visualising the data in layman terms to provide a definitive perspective to the users. 

**Inferential Statistics** involves learning to make a prediction from the given data or extract information with unusual patterns that can prove to be useful in decision making. It is concerned with population parameters from a sample.

For example, studying the stock market prices in order to predict the prices of the future, and perform risk analysis in order to determine the optimal amount to be invested to maximise profits and prevent loss of investments.

There is also a third category called '**Prescriptive Statistics**'. This is used in presribing the test subject with a treatment to affect behaviour of the subject and observe the results to get better interpretations that can be applied to the population.

For example, a doctor treating a set of patients with a certain illness and he tries different treatment to each patient for a week to observe how they react to the treatment, and whichever gets the best results then that treatment is recommended or 'prescribed' to the others who are having similar symptoms.

## Data Types
The first major form of different types of data is in terms of structured and unstructured data. We are concerned with structured data more that has an organized nature and can be used to extract meaningful information and extract patterns from it.

A broad distinguishing feature of data is in terms of its measurement.
- Qualitiative: The data that is non-numeric by nature and cannot be measured is called qualitative data.
- Quantitative: The data that is numerical by nature and is measurable is called quantitative data. It can be classified into discrete and continous types of data.

Hence, we will now get into details of the different types of such data.

- Continous: Data that can take on any interval
- Discrete: Data that can take on any integer value
- Categorical: Data that can take a specific set of values representing a set of possible categories
- Binary: Data with only two possible categories or values ie 0/1 or True/False
- Ordinal: Categorical Data that has explicit ordering

Examples:
- Continous Data: Wind speed, time durations
- Discrete Data: Count of occurences of an event, number of persons in a population
- Categorical Data: List of states in a country
- Binary Data: Gender: Male or Female, Email Spam/not Spam
- Ordinal Data: T-shirt sizes: S, M and L

![alt-text](https://raw.githubusercontent.com/vgaurav3011/Statistics-for-Machine-Learning/master/images/data_types.png)

## Why do we need to classify data into different types?

- Storage and indexing can be optimized
- The possible values of a categorical variable can be enforced in a software (eg. enum)
- Knowing the nature of the data can help us plot a visual or fit a model

## Key Terms in Statistics

1. Population: The total number of possible data points present in the data is called its population.
2. Sample: A subset of the population selected in such a way that it preserves the variance of the population and exhibits same behaviour when subjected to operations much like the overall population.
3. Statistic: It is a numerical value associated with an observed sample.
4. Parameter: It is a numerical value associated with a population.

Now, why are we learning statistics?? Our aim is to get information from raw data.

**Raw Data** represent numbers and facts in the original format in which the data have been collected. We need to convert the raw data into information for decision making.

When we mine useful patterns after structuring this data, we get the data in form of **information**.

## Estimates of Location

1. Mean: The sum of all values divided by the number of values.
2. Weighted Mean: The sum of all values times the weight of each observation in the data.
3. Median: The middle value of data, in case of even number of terms we take the average of the two middle values present in the data.
4. Weighted Median: The value such that one half of the sum of weights lies above and other half lies below the sorted data.
5. Trimmed Mean: The average of all the values after dropping a fixed number of extreme values.
6. Robust: Not sensitive to extreme values.
7. Outlier: A datapoint which exhibits different behaviour from the majority of data points in the population.

- Mean = $^1/_N$ $\sum_{i=1}^{n} x_i$
where N = Total number of records or Population
	    n = Total number of records in Sample
	    and n is a subset of N
	
- Note: Mean is known to be prone to outlier or extreme values
For example, we are calculating the average of incomes of persons sitting in a restaurant with lowest income being $100 and highest being $500, and mean income is nearly about $300. Suddenly, Bill Gates enter the restaurant and takes a seat. His income is $1 billion (assume), so now the new mean will be approximately a billion which is way higher than incomes of others in the same dataset or population. Hence, mean is sensitive to outliers.

- Thus, we use a trimmed mean as described which drops these extreme values.
Trimmed Mean = $^1/(_N-2p)$ $\sum_{i=p+1}^{n-p}x_i$ where p are the extreme values on both sides of the data.

- Weighted Mean = $\sum_{i=1}^{n}w_i.x_i$ / $\sum_{i=1}^{n}w_i$ is used when the data does not represent all the groups equally and some variables are more intrinsic than other variables and need to be given higher weights as a result.
- Median: 
	- Sort the values in ascending order
	- If the number of terms is odd, then take the middle value
	- If the number of terms is even, then take the average of the middle values
	Median is a robust estimate because it is not affected by outliers
