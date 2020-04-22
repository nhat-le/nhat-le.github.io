---
layout: post
title: "Overfitting revisited"
date: 2020-04-20
---

In this post, I'm going to tell you some new and potentially interesting perspectives on overfitting and underfitting. I learned most of the materials in this post from a recent talk by Professor Mikhail Belkin at the Ohio State University, so all the credits go to him. Here, I try to explain his results in a way that makes the most sense to me. Hopefully you will find this post interesting too.

![Overfitting](http://nhat-le.github.io/files/overfitting.png)

Now, let's dive in. Let's start with the concept of *overfitting*. (If you're already familiar with overfitting, feel free to skip this section) Let's say, for example, that you're given a bunch of data points (shown in blue) and are asked to draw a best-fit line through these points.

What sort of line would you draw? Well, you could start with a very simple model, a straight line. A straight line could capture some of the variation you see, but not much. We call this *underfitting* - the model is too simple to describe the data satisfactorily.

We can increase the complexity of the model. Perhaps try a quadratic function, or a degree 4 polynomial. When we try to fit a degree 4 polynomial to the data, we do substantially better. The curve looks reasonable now...

But what if we try to fit a very complex model, say a 15-degree polynomial? At a first glance, we seem to do even better than before - our line now passes through most of our data perfectly! If we evaluate our model based on how far it deviates from training data, this model should make us happy since our error is quite small. So why are we uneasy about this result?

Well, one reason is that we are doing well on the training data, but what we have done is fitting to the noise inherent in our dataset instead of capturing the variation in the data. Our model would perform quite poorly on dataset it has not seen before. We say that there is substantial *overfitting* in the model.







**Now comes the strange stuff...**

When performing data analysis, you often need to regress your data \\(y\\) against some regressors. If you're familiar with machine learning and regression, you have probably seen this plot:

The plot shows what happens when you try to fit a very complex model to your data: you get massive overfitting and do poorly on a held-out dataset.

Now the question is, *what will happen if you increase the complexity of the model even more?* 

Of course, you may say, the test error will just get worse! The textbook tells us, when we try to fit a complex model with many parameters to a simple dataset, we can't expect to do well.

Well, it turns out we can.

[To be continued...]

Here is the link to Professor Belkin's paper for those interested: [PNAS](https://www.pnas.org/content/116/32/15849.short)
