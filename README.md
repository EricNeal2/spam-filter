# Spam Filter
Building a spam filter for SMS messages using the Multinomial Naive Bayes algorithm. I used a dataset of 5,572 messages from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection).


## Summary
- **Train and Test data**: Use 80% of the messages to train the filter, and 20% to test its accuracy.
- **Data Cleaning**: Create a column for each word found in the training data, where the values are integers corresponding to the number of occurences of that word in the given message.
- **Calculate Constants and Parameters**: Use the training data to calculate all the constants and parameters needed for the Naive Bayes algorithm (P(Spam), P(Ham), N<sub>Spam</sub>, N<sub>Ham</sub>, N<sub>Vocabulary</sub>, P(w<sub>i</sub>|Ham), and P(w<sub>i</sub>|Spam)).
- **Classifiying a Message**: Write a function that takes a message and using the Naive Bayes Algorithm, classifies the message as either ham or spam. Apply this function to the test data, and measure the accuracy of the filter.

## Results

The accuracy of the spam filter on the test data was 98.7%. It correctly classified 99.4% of the ham messages, and 94.6% of spam messages.

I am happy with the performace of the filter, as I think it's more important to correctly classify ham messages. Personally, I would be fine with a few spam messages slipping through the filter as long as it means none of the real messages from my friends get blocked.
