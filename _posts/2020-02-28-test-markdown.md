---
layout: post
title: Implementation of Kriging Convolutional Networks
subtitle: Application of GNN and Kriging to Spatial Interpolation
gh-repo: daattali/beautiful-jekyll
gh-badge: []
tags: [Graph Nerual Network, Torch, Torch Geometric]
comments: false
---

### Overview

I lead the PyTorch implementation of Kriging Convolutional Networks (KCNs) [1]. There was an old implementation with TensorFlow 1.x, which is not well supported now. In this project, we update the implementation with PyTorch and PyTorch Geometric. We hope this new implementation will help researchers in this field. 

We make some modifications to the model and conduct parameter fine-tuning to increase model performances on different datasets. Performances improved when tested on different datasets. The performance increases from 0.50/0.49/0.44 to 0.46/0.45/0.44 when running on a dataset of bird counts[2].(The three results correspond to the constructions of KCNs using GCN, GAT, GraphSAGE.)

We also make adjustments from an engineering perspective to improve the speed of model training.

**Github : [https://github.com/tufts-ml/kcn-torch#a-pytorch-implementation-of-kriging-convolutional-networks]**

### Kriging Convolutional Networks

A KCN predicts a data point's label based on data points in its neighborhood. The KCN model stores a training set internally. To make a prediction for a data point, it looks up neighbors for the data point and construct, forms an attributed graph over data points in the neighborhood, and then uses a Graph Neural Network (GNN) to predict the data point's label. During training, these graphs are computed before training to save repeated graph constructions. The general structure of KCN is similar to a k-nearest-neighbor classifier, though the former one employs a much more flexible predictive function than simple averaging.

In the implementation, a KCN model is a PyTorch module. It is initialized with a SpatialDataset. In the forward function, it takes coordinates and features of a batch of data points and then predicts their labels.

### References

[1] Gabriel Appleby, Linfeng Liu, and Li-Ping Liu. "Kriging convolutional networks." Proceedings of the AAAI Conference on Artificial Intelligence. Vol. 34. No. 04. 2020.   
[2] Sullivan, B.L., C.L. Wood, M.J. Iliff, R.E. Bonney, D. Fink, and S. Kelling. 2009. eBird: a citizen-based bird observation network in the biological sciences. Biological Conservation 142: 2282-2292.

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
