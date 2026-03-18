# Evaluation Limits

The evaluation results suggest that the sentiment model performs reasonably well at first glance, but closer analysis reveals several limitations. While the model correctly classified seven out of ten examples, the confusion matrix shows a clear pattern of errors.

The confusion matrix indicates that three positive quotes were misclassified as negative. This suggests that the model tends to interpret certain keywords, such as “failed”, “stupid”, or “hated”, as strong negative signals even when the overall meaning of the sentence is motivational or humorous.

Another issue is that incorrect predictions are often made with very high confidence scores. For example, the quote “I have not failed. I've just found 10,000 ways that won't work.” was classified as negative with a confidence score of 0.997. This demonstrates that confidence values can give a misleading impression of reliability.

The model also struggles with figurative language and rhetorical tone. Many quotes in the dataset use metaphor or humour to express positive ideas. However, the system tends to interpret individual words literally rather than understanding the overall context of the sentence.

The toxicity analysis shows a similar limitation. The quote containing the word “stupid” received a very high toxicity score (0.868) despite being a literary expression rather than a direct insult. This suggests that the model relies heavily on keyword detection rather than contextual interpretation.

When evaluation metrics are aggregated, these patterned failures become less visible. A relatively high overall accuracy can hide systematic weaknesses in handling metaphor, humour, and inspirational language. As a result, users who rely on nuanced or figurative communication are the most likely to be misled by the system.