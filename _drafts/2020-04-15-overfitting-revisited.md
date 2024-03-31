---
layout: post
title: "Overfitting revisited"
date: 2020-04-20
---

In this post, I'm going to tell you some new and potentially interesting perspectives on overfitting and underfitting. I learned most of the materials in this post from a recent talk by Professor Mikhail Belkin at the Ohio State University, so all the credits go to him. Here, I try to explain his results in a way that makes the most sense to me. Hopefully you will find this post interesting too.

Now, let's dive in. Let's start with the concept of *overfitting*. (If you're already familiar with overfitting, feel free to skip this section) Let's say, for example, that you're given a bunch of data points (shown in blue) and are asked to draw a best-fit line through these points.

![Overfitting](http://nhat-le.github.io/files/overfitting.png)

**Figure 1** Underfitting and overfitting [1]


What sort of line would you draw? Well, you could start with a very simple model, a straight line. A straight line could capture some of the variation you see, but not much. We call this *underfitting* - the model is too simple to describe the data satisfactorily.

We can increase the complexity of the model. Perhaps try a quadratic function, or a degree 4 polynomial. When we try to fit a degree 4 polynomial to the data, we do substantially better. The curve looks reasonable now...

But what if we try to fit a very complex model, say a 15-degree polynomial? At a first glance, we seem to do even better than before - our line now passes through most of our data perfectly! If we evaluate our model based on how far it deviates from training data, this model should make us happy since our error is quite small. So why are we uneasy about this result?

Well, one reason is that we are doing well on the training data, but what we have done is fitting to the noise inherent in our dataset instead of capturing the variation in the data. Our model would perform quite poorly on dataset it has not seen before. We say that there is substantial *overfitting* in the model.

In fact, if we plot our training and test error against model complexity, we get something like this 

![Bias-variance](http://nhat-le.github.io/files/bias_variance.png)

**Figure 2** The bias-variance trade-off [2]

To the left of the plot, our models are underfitting, as training and test errors are both high. We fail to capture most of the variation even in the training data. To the right, our models are overfitting - our training errors are quite small, but the test errors are increasing rapidly... This kind of plot is the famous *bias-variance* trade-off we typically see in a statistical learning class.



**Now comes the strange stuff...**

Ok, ready for some new stuff? Let me ask you following question: *What will happen if we increase the complexity of the model **even more?** * 

You must be kidding me! You say. In the previous section, you showed me the bias-variance trade-off plot, and you tell me that if we go towards the right hand side, training error will continue to decrease and test error will continue to rise. We must be massively overfitting if we increase the complexity even more! 

That was what I thought, until I went to the talk by Professor Mikhail Belkin...

[To be continued...]

Here is the link to Professor Belkin's paper for those interested: [PNAS](https://www.pnas.org/content/116/32/15849.short)

References
[1] https://scikit-learn.org/stable/auto_examples/model_selection/plot_underfitting_overfitting.html
[2] https://www.researchgate.net/publication/222344717_Spatial_prediction_of_soil_properties_in_temperate_mountain_regions_using_support_vector_regression
