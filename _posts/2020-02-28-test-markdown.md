---
layout: post
title: Implementation of Kriging Convolutional Networks
subtitle: Application of GNN and Kriging to Spatial Interpolation
gh-repo: daattali/beautiful-jekyll
gh-badge: []
tags: [Graph Nerual Network, Torch, Torch Geometric]
comments: false
---

I lead the PyTorch implementation of Kriging Convolutional Networks (KCNs) [1]. There was an old implementation with TensorFlow 1.x, which is not well supported now. In this project, we update the implementation with PyTorch and PyTorch Geometric. We hope this new implementation will help researchers in this field. 

We made some modifications to the model and conducted parameter fine-tuning to increase their performances on different datasets. Performances improved when tested on different datasets. The performance increases from 0.50/0.49/0.44 to 0.46/0.45/0.44 when running on a dataset of bird counts[2].(The three results correspond to the construction of kcn using GCN, GAT, GraphSAGE.)

**Github : https://github.com/tufts-ml/kcn-torch#a-pytorch-implementation-of-kriging-convolutional-networks**

## Kriging Convolutional Networks

Here's a useless table:

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
