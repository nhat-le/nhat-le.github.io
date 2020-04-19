---
layout: post
title: "Strange Regression"
date: 2020-04-20
---

In this post, I'm going to talk about a very strange phenomenon in regression that involves overfitting and underfitting. I learned about this strange phenomenon at a recent CBMM meeting. The presentation was by Professor Mikhail Belkin at the Ohio State University. I was expecting a difficult presentation filled with complex math, but the following idea stood out to me.

When performing data analysis, you often need to regress your data \\(y\\) against some regressors. If you're familiar with machine learning and regression, you have probably seen this plot:

The plot shows what happens when you try to fit a very complex model to your data: you get massive overfitting and do poorly on a held-out dataset.

Now the question is, *what will happen if you increase the complexity of the model even more?* 

Of course, you may say, the test error will just get worse! The textbook tells us, when we try to fit a complex model with many parameters to a simple dataset, we can't expect to do well.

Well, it turns out we can.

[To be continued...]

Here is the link to Professor Belkin's paper for those interested: [PNAS](https://www.pnas.org/content/116/32/15849.short)
