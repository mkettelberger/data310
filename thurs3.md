###***Country Persons Dataset***

This large dataset contained about 48,219 different data points with 15 distinct features including
numerical columns such as age, size, and weight and categorical columns such as toilet, location,
and potable water. When first dealing with the data, I dropped 3 columns (hhid, pnmbr, and unit), and 
I removed all of the rows that had missing or unknown information. Usually, these were 
represented by the numbers 8 or 9, but if the feature was comprised of strings, I was able to remove it 
by using the keyword 'Missing'. After setting the target to wealth, I also manipulated the 'electric' and
'car' columns to turn them into integers instead of strings. Every value that was equal to 'No', I set to
0 and every other value I made 1.

When choosing the columns for my features, I tried many different combinations, but most returned very
similar results. Combinations I tried included:



Numeric = weights, size, age

Categorical integers = gender, education

Categorical strings = location, potable, toilet, cook, electric, car (before these were turned into numbers)


----------------------------------------------------------------------------------------------


Numeric = weights, size, age, **education**

Categorical integers = gender

Categorical strings = location, potable, toilet, cook, electric, car (before turned to numbers)

--------------------
*This is the one I used for other wealth value tests*

*Numeric = weights, size, age*

*Categorical integers = gender, **education, electric, car***

*Categorical strings = location, potable, toilet, cook*

---------------------------------

Numeric = weights, size, age, **education**

Categorical integers = gender, electric, car

Categorical strings = location, potable, toilet, cook

-------------------------------------

In an attempt to get better accuracies, I played around with the batch size
(decreasing it to 128 and 64), the dropout rate (increasing it to 0.8 and lowering to 0.2),
and adjusting the epochs all the way up to 50. I also tried to change the optimizer
to tf.keras.optimizers.SGD(learning_rate=0.01), but the results stayed the same.

After all of these adjustments, I tested the other values of wealth (I had been using 2 as the
chosen value up until this point). As I increased the values (1-5) the accuracy became
better and better. Based on the 256 batch size and 10 epochs here were my results:


Wealth = 1

Accuracy = 0.7964

-------

Wealth = 2

Accuracy = 0.7435

----

Wealth = 3

Accuracy = 0.7923

---

Wealth = 4

Accuracy = 0.8852

---

Wealth = 5

Accuracy = 0.9636

---

As one can see, 4 and 5 had much better accuracies probably because the values of the features for these targets
were much more separated from the rest of the wealth classifications and had clearer patterns. In addition,
when wealth was 1, it did better than 2 or 3 because it was the lower bound of the data
and would not get mislabeled as much.

For the future, I wanted to try bucketizing the columns, but my code wasn't running with those lines, and I think
it would be a good idea to find what type of examples the model was consistently mislabeling
to try and minimize that. Trying more different optimizers could also be helpful.



