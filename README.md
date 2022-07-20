# Amazon Vine Analysis

#### Overview of the analysis:

In this project we have the analyzing Amazon reviews written by members of the paid Amazon Vine program task. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project we made a ETL process with Pyspark to extract the Beauty dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we used PySpark,  to determine if there was any bias toward favorable reviews from Vine members in our dataset.

#### Results: 

### How many Vine reviews and non-Vine reviews were there?
To get to this point we first had to filter our database so that it had the right information for our analysis.

- First we filter so that we have equal or more than 20 votes per ID. This was done to have useful and positive information for the following mathematical procedures.

- Then we filter so that we have the percentage of the number of useful votes of the total votes for each Id.

- Finally we obtained the information of the total and by rating of 5 stars for the paid and unpaid reviews.


With the above, we obtain the following findings:

![Picture One](https://github.com/LAURYMEOW/Amazon_Vine_Analysis/blob/main/Resources/Table.png)

Of a total of 74,760 reviews, 647 were paid and 74,113 were not.

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

Of the 647 paid reviews, only 229 had a 5-star rating, while of the 74,113 reviews obtained outside the program, 43,217 had the maximum rating.

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

That is, of the total reviews, 58% of the data obtained 5 stars, of which 35% came from the Vine program and 58% were independent.

![Picture 2](https://github.com/LAURYMEOW/Amazon_Vine_Analysis/blob/main/Resources/Picture_chart.png)


#### Summary:

With the above, it can be concluded that there was no type of bias for the reviews due to the application of the Vine program in this category (Beauty).
We can trust that reviews are telling us relevant information about how satisfied customers are with the products they have purchased.
It can also seen that the paid reviews was sincere and critical, which are very useful to improve the evaluated product.

Bearing this information in mind, we can go on to make a more detailed analysis to find out the products that are most in demand and most accepted by consumers, as well as those that have been totally rejected.

With this information we can carry out marketing campaigns for the sale of outstanding products and promote the improvement of non-excellent products.
