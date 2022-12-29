# SentimentAnalyzer

"""
The output of get accuracy on the test examples are:
Positive accuracy: 0.960431654676259
Negative accuracy: 0.7043795620437956
Total accuracy: 0.9098124098124099

The model overall accurately calculates whether a file consists of negative reviews or positive reviews.
We can see that the positive accuracy is 0.96, so it predicts if a statement is positive 96% of the time.
The negative accuracy is 0.7, which means that it predicts if a statement is negative 70% of the time.
The model is better at predicting whether a statement is positive as opposed to if a statement is negative.
However, since the overall accuracy is 0.91, or 91%, we can see that the model is pretty accurate at predicting.

Wrong guesses:

1) "I hate my marriage, I think it is not the best" - the model predicts this negative statement as positive.
2) "I do not want people dying" - the model predicts this positive statement as negative.

For 1, the reason why the model makes a mistake is because the probability of the word "hate" (0.00539568345323741)
outweighs the overall probability of the other words in the sentence excluding hate (1.380267367641113e-09). For
this example, I trained the test.positive file using the train model function and then used the get_probability
function to find the probabilities of each word in a given string. For 2, the words "do not" have a higher 
probability (0.012906920986733444) than the remaining words in the sentence (9.576281436271099e-08). So, these 
two words cause the overall positive statement to be predicted as negative. For this example, I trained 
the test.negative file using the train model function and then used the get_probability function to get the 
probabilities of each word in a given string.
"""
