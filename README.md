# Poet Detecotor
This project is an **NLP** Project to recognize the poet of a poem. The training set consists of some poems from Molavi, Hafez and Ferdowsi. At first, we created a dictionary from all words that occurred more than **two** times in the training set. We then created the **unigram** and **bigram** model for each of the poets by calculating the probabilities and then applied the backoff model for smoothing. 


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![](https://latex.codecogs.com/png.latex?\dpi{100}&space;\fn_jvn&space;\large&space;P\left&space;(&space;c_{i}\mid&space;c_{i-1}&space;\right&space;)&space;=&space;\lambda&space;_{3}P\left&space;(&space;c_{i}\mid&space;c_{i-1}&space;\right&space;)&space;&plus;&space;\lambda&space;_{2}P\left&space;(&space;c_{i}&space;\right&space;)&space;&plus;&space;\lambda&space;_{1}\epsilon)

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![](https://latex.codecogs.com/png.latex?\dpi{100}&space;\fn_jvn&space;\large&space;\lambda&space;_{3}&space;&plus;&space;\lambda&space;_{2}&plus;&space;\lambda&space;_{1}&space;=&space;1)


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![](https://latex.codecogs.com/png.latex?\dpi{100}&space;\fn_jvn&space;\large&space;0&space;<&space;\epsilon&space;<1)

We applied the generated model to the test set. The test set consists of poems matched by a number to show each poem belongs to which of the poets. We could gain **87** percent accuracy in predicting the correct poet on the test set poems.
