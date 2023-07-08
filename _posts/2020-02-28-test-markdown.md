---
layout: post
title: Implementation of Kriging Convolutional Networks
subtitle: Application of GNN and Kriging to Spatial Interpolation
gh-repo: daattali/beautiful-jekyll
gh-badge: []
tags: [Graph Nerual Network, Torch, Torch Geometric]
comments: false
---

This repo contains the PyTorch implementation of Kriging Convolutional Networks (KCNs) [1]. The original code release was an implementation with TensorFlow 1.x, which is not well supported now. In this repo, we update the implementation with PyTorch and PyTorch Geometric. We hope this new implementation will help researchers in this field. If you have any questions about this repo, please feel free to raise issues.

**[Github:](https://github.com/tufts-ml/kcn-torch#a-pytorch-implementation-of-kriging-convolutional-networks)**

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
