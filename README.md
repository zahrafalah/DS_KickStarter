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