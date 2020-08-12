"The KNN algorithm assumes that similar things exist in close proximity. [...] KNN captures the idea of similarity by calculating the distance between points on a graph."
  - most common: euclidiean disctrance

![close](https://miro.medium.com/max/611/1*wW8O-0xVQUFhBGexx2B6hg.png)

e.g.; a 33 year old thinks similarly to a 31 year old or 35 year old, so if we are interested in what a 33 year old thinks (query value) then we look for K people that are "most similar" to our query value (aka 31 year old, 35 year old). This similarity is measured by the distance between the ages. Once we calculate the distances from our query value to each of the data points, we get the K closest (most accurate). We then look at the labels to determine our output (if we have classificatino problem, take mode of the labels; for regression, take mean)
