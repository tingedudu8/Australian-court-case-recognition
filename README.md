# Australian-court-case-recognition

## Important Considerations

1. To get good accuracy, I have centered and normalized the data. That is, transform my data so that the mean of each dimension is zero, and the standard deviation is one. That is, subtract the mean vector from each data point, and then divide the result by the vector of standard deviations computed over the data set.

2. To avoid overﬂow problems, both when computing the LLH and when computing the gradient update. Some things I do to avoid this are, (1) use np.exp() which seems to be quite robust, and (2) transform my data so that the standard deviation is smaller than one. I experiment a bit. Such are the wonderful aspects of implementing data science algorithms in the real world!

3. Training my model on a small sample of the large data set (say, 10% of the documents) then using the result as an initialization, and continue training on the full data set. This speeded up the process of reaching convergence.


## Accuracy Test
![这是图片](/images/Accuracy.png)


