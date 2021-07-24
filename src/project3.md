# Project 3

- Using either the [Classify structured data with feature columns](https://www.tensorflow.org/tutorials/structured_data/feature_columns) script or the [Classify structured data using Keras Preprocessing Layers](https://www.tensorflow.org/tutorials/structured_data/preprocessing_layers) with the `country_persons.csv` dataset, specify, train and evaluate models that predict class of wealth versus all other classes as a binary target.  Amongst the five possible binary targets (1 versus all others, 2 versus all other etc...), produce your results from the two models with the best and worst accuracy.

- Using the data and two models you produced in step 1, create a confusion matrix.  You are welcome to use the following script.  With your confusion matrix as a reference, analyze and discuss the two sets of results you produced.

- Again using either the [Classify structured data with feature columns](https://www.tensorflow.org/tutorials/structured_data/feature_columns) script or the [Classify structured data using Keras Preprocessing Layers](https://www.tensorflow.org/tutorials/structured_data/preprocessing_layers) with the `country_persons.csv` dataset, specify, train and evaluate a model that predicts all class of wealth outcomes as a categorical target.  Again create a confusion matrix in order to analyze and discuss your results.  Revisit the [Classify structured data with feature columns](https://www.tensorflow.org/tutorials/structured_data/feature_columns) script or the [Classify structured data using Keras Preprocessing Layers](https://www.tensorflow.org/tutorials/structured_data/preprocessing_layers) in order to modify your feature columns, in attempt to improve the accuracy of your model that uses all five categorical wealth classes as the target.  Analyze and discuss your progress and results.

### Step 1.  Define your confusion matrix plot command

```
# confusion matrix

def plot_confusion_matrix(cm, classes,
                          normalize=False,
                          title='Confusion matrix',
                          cmap=plt.cm.Blues):
  """
  This function prints and plots the confusion matrix.
  Normalization can be applied by setting `normalize=True`.
  """
  import itertools
  if normalize:
    cm = cm.astype('float') / cm.sum(axis=1)[:, np.newaxis]
    print("Normalized confusion matrix")
  else:
    print('Confusion matrix, without normalization')

  print(cm)

  plt.imshow(cm, interpolation='nearest', cmap=cmap)
  plt.title(title)
  plt.colorbar()
  tick_marks = np.arange(len(classes))
  plt.xticks(tick_marks, classes, rotation=45)
  plt.yticks(tick_marks, classes)

  fmt = '.2f' if normalize else 'd'
  thresh = cm.max() / 2.
  for i, j in itertools.product(range(cm.shape[0]), range(cm.shape[1])):
    plt.text(j, i, format(cm[i, j], fmt),
             horizontalalignment="center",
             color="white" if cm[i, j] > thresh else "black")

  plt.ylabel('True label')
  plt.xlabel('Predicted label')
  plt.tight_layout()
```

### Step 2. Create objects that describe the true and predicted target values

```
y_true = assign the true target values to this object
y_pred = assign the predicted target values to this object
```

### Step 3. Plot your confusion matrix

```
cnf_matrix = confusion_matrix(y_true, y_pred,labels=[add labels here])
np.set_printoptions(precision=2)

plt.figure()
plot_confusion_matrix(cnf_matrix, classes=[add labels here],
title='title your plot')
plt.show()
```