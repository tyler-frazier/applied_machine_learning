# Wednesday

## Start with the *Basic classification: Classify images of clothing* script that you prepared for today's class.  Execute the following.

- From the *Preprocess the data* section of the script, modify the training image to produce three new images.
- Under the *Make predictions* section, present the array of predictions for an image from the test set other than the one given in the example script.  What does this array represent? How were the `Softmax()` and `argmax()` functions applied?  Read this post from DeepAI, [What is the Softmax function](https://deepai.org/machine-learning-glossary-and-terms/softmax-layer) for a description of the two functions (focus on the softmax formula, calculating softmax and the softmax vs. argmax sections).  Does the output from `np.argmax()` match the label from your `test_labels` dataset?
- Under the *Verify predictions* section, plot two additional images (other than either of the two given in the example script) and include the graph of their predicted label as well as the image itself.
- Under the *Use the trained model* section, again select a new image from the test dataset.  Produce the predictions for this newly selected image.  Does the predicted value match the test label?  Although you applied the `argmax()` function in this second instance, you did not use `Softmax()` a second time.  Why is that so (please be specific)?

## Copy the script you produced for the Fashion MNIST dataset.  Modify the script as follows and produce the following output.

- Change the line 

```
fashion_mnist = tf.keras.datasets.fashion_mnist
```

to 

```
mnist = tf.keras.datasets.mnist
```

in order to switch the dataset from sets of clothing to hand written numbers.  Produce a plot of 25 handwritten numbers from the data with their labels indicated below each image.  Fit the model and report the accuracy of the training dataset.  Likewise report the accuracy of the test dataset.  As in the above example, from the *Verify predictions* section, plot two  images and include the graph of their predicted label as well as the image itself.
- Evaluate how your model for the MNIST dataset compared with your model of the Fashion_MNIST dataset.  Which of the two models is more accurate?  Why do you think this is so?

## For Thursday's class, reproduce the script on [Basic Text Classification](https://www.tensorflow.org/tutorials/keras/text_classification).  Please read through the script and confirm you are able to execute a basic inferential sentiment analysis.







