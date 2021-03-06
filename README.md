# Apriori
Improving the efficiency of Apriori Algorithm to work with humongous datasets

Apriori is an algorithm for frequent item set mining and association rule learning over relational databases. It proceeds by identifying the frequent individual items in the database and extending them to larger and larger item sets as long as those item sets appear sufficiently often in the database. 
 
Using Apriori algorithm to find the frequent items for a large dataset is very difficult using the pre-existing python libraries. These libraries load the complete dataset on the memory at a time which freezes the operation at that instance and ultimately makes the system very slow. The output generation time rises exponentially per 1000 entries after 1,00,000 entities. Hence the existing models can’t be used for deriving output in case humongous dataset.

Python Generators

Now, division of dataset failed to fulfill our need. Here comes Python Generators in the picture. In a nutshell, a generator is a special type of function that returns an iterable sequence of items. However, unlike regular functions which return all the values at once (e.g.: returning all the elements of a list), a generator yields one value at a time. To get the next value in the set, we must ask for it - either by explicitly calling the generator's built-in "next" method, or implicitly via a for loop. This is a great property of generators because it means that we don't have to store all of the values in memory at once. We can load and process one value at a time, discard when finished and move on to process the next value. This feature makes generators perfect for creating item pairs and counting their frequency of co-occurrence. Now, getting item pairs, one at a time, doesn’t overload the memory at any point of time. Now, the problem of memory over load is taken care of. This in turn takes care of speed as well. Now each generated pair is used to calculate all the metrics like Support, Confidence and Lift. This is saved in the output variable. This process takes place on the fly; hence no memory is engaged for saving things. This makes the overall functioning faster and helps achieving our output efficiently and accurately.

Data Source: https://www.kaggle.com/c/instacart-market-basket-analysis/data
