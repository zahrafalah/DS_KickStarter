# DS_KickStarter

### `Sorting and Filtering Data`
One of the simplest ways we can start to explore data is to sort it by fields
that we think are important, and to filter the data to show only the records
of interest. For example here's Rosie's lemonade data and it's sorted by date.
Now Rosie could sort the lemonade sales data by the number of sales per day like this.
Now notice that the whole dataset is now sorted in ascending order by sales, and
the days on which Rosie made the fewest sales are first. Of course she can also
sort the data by sales in descending order so that the days on which she made
the most sales appear first. Now suppose Rosie sorts the data into
descending order of flyers so the days on which she distributed most flyers
appear first; and if we look at the data closely you can see something that might
be a little odd. The most flyers Rosie distributed in one day was 99, but
there's a big gap to the next highest value. We call values like this, that are
unusually high or low compared to the rest of the data, outliers; and they can
affect the analysis of the data as we calculate aggregations and summary
statistics. Now it may be that on one day Rosie genuinely did distribute an
extremely high number of flyers; or it may be a mistake maybe she mistyped
19 as 99; we don't know, but it's good to be aware of the existence of extremes
and outliers as we continue to analyze the data.
Let's resort the data into date order and then filter it to show only
Saturdays and Sundays. This removes the other rows so we can focus on how
Rosie's lemonade stand performed on weekends. You can filter the data based
on any criteria. In this case the criteria is the day must be Saturday or
Sunday, but we could also filter on numeric comparisons for example to show
only days where the temperature is below 30 degrees.



 ### `Aggregating data`
  is usually the first kind of analysis you perform in order to summarize the data and get a feel for it as a whole. One of the first things you might want to ascertain is how many records are in the data set. This is known as the count. Now
you can calculate the count for any kind of column, not just numeric columns. It just tells you how many rows there are. For categorical data, you might want to calculate something called the distinct count; which counts how many distinct values that are. In this case, the data set includes sales data for seven
discrete days of the week. The total, or sum, is a common aggregation of interest.

### `Grouping and Summarizing Data`
When your dataset includes categorical values, it's common to group the data by
categories and calculate subtotals for numeric values.

 ### `Measuring Central Tendency`

 Statistical analysis is at the core of data science. Using statistics, you can learn about the distribution of the data, how much of variance there is between values, and how values for one feature of the data I seem to influence other
values. The starting point for learning how to use statistics to analyze data is to understand the common descriptive statistics that we can use to understand the distribution of our data.(Min, Max, Mean, Median, Mode). A histogram, and it shows the frequency of data values within distinct ranges, or bins; and in this case each bin covers a range of ten values. Note that the mode, being the most frequent value, causes a peak in the data set; and in this case the mean median and mode are all more or less centrally located, with symmetric tails on the left and right showing progressively fewer values for more extreme temperatures.
When data is distributed as a bell curve like this, we call a normal distribution; and statisticians love to work with normally distributed data like this for a number of reasons, some of which we'll explore later. Another way you can visualize the distribution of your data is to use a box and whiskers plot. In this case the box in the center represents the inner two quartiles of the data, with the median showing as a line. in Excel you can also display the mean as an X.
The whiskers show the rest of the data to the minimum and maximum. You can show a box and whisker chart in this horizontal orientation, but often, especially in Excel, it's shown in this vertical view. `Measuring Variance`: We indicate the population variance as Sigma-squared. We calculate the square root of the
variance to calculate something called the standard deviation.  In a normal distribution the mean is in the middle
and around 68.26% of all observations lie within one standard
deviation above or below the mean. Around 95.45% of observations
lie within two standard deviations of the mean;
and around 99.73% of observations lie within three standard deviations of the
mean. So by knowing the mean and the standard deviation, we get a pretty good
idea of how the data in our sample is distributed, allowing for variances in
the values.
 ### `Working with Samples`
  Generally you work with samples of data that are representative
of the data, and you use sample statistics such as the mean and standard
deviation to approximate the parameters of the full data population. what can we do to ensure our sample statistics are truly representative of
the full population parameters. Well up to now we've used fairly small sample
sizes. In practice it's best to get as large a sample as you can. The larger the
sample, the better it will approximate the distribution and parameters of the
full population. Another thing you can do is to take multiple random samples. Each
sample has a sample mean, and you can record these to form what's called a
sampling distribution. With enough samples, two things happen. One is that,
thanks to something called the central limit theorem, the sampling distribution
takes on a normal shape regardless of the shape of the population distribution;
and the second thing is that the mean of the sampling distribution, in other words
the mean of all the sample means, will be the same as the population mean.

### `Correlation`
So far we've talked about descriptive statistics that help us understand the
distribution of values in a data set, and we've seen how to work with samples and
use statistics as approximations for full population parameters. let's examine how we can use statistics to find relationships between
different fields in our data. 
 But can we quantify
this relationship? Well yes, we can calculate a statistic called correlation
and in Excel you do it using the Correl function. Correlation is a value between
negative 1 and positive 1 that indicates the strength and direction of a
relationship. A value near positive 1 indicates a positive relationship in
which an increase in one value generally correlates with an increase in the other. A
value near negative 1 on the other hand indicates a negative correlation in
which an increase in one value tends to be associated with a decrease in the
other value.  Now it's important to remember that correlation
is not the same thing as causation.
This statistic shows us that high sales tend
to occur on days with high temperatures, but that doesn't necessarily prove that
Rosie sells more lemonade because it's hot. The statistics could just as easily
be used to claim that the more lemonade Rosie sells the hotter it gets!

### `Machine learning`
Machine learning is a way of using data to train a computer model so that it can
predict new data values based on known inputs. The model learns from training
cases, and we can then use that trained model to make predictions for new data
cases. Now the key to understanding this is that fundamentally computers are very
good at one thing - performing calculations; and in fact the earliest
computers were known as calculation engines. To have a computer make
intelligent predictions from data, we just need a way to train it to perform
the correct calculations. So we start with a data set that contains historical
records, often called cases or observations. Each observation includes
numeric features that quantify a characteristic of the item that we're
working with. So let's call this X. In general, we also have some value that
we're trying to predict; let's call this Y. We use our training cases to train a
machine learning model so that it can calculate a value for Y from the
features in X. So in very simplistic terms, what we're doing is creating a
function that operates on a set of features X, to produce predictions Y.
Generally speaking, there are two broad kinds of machine learning: supervised and
unsupervised. In supervised learning scenarios, we start with observations
that include known values for the variable we want to predict. We call
these labels. Then we use a machine learning algorithm to train a model that
fits the features to the known label. Because we started with a known label
value, we can validate the model by comparing the value predicted to the
actual label value that we had in the first place; then when we're happy that
the model works we can use it with new observations for which the label is
unknown and generate new predicted values. Unsupervised learning is
different from supervised machine learning in that we don't have a known
label in the training data set. We train the model by finding similarities in the
observations.
After the model is trained, each new observation is assigned to a cluster of
observations with similar characteristics.

