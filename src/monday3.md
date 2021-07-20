# Monday

Start with the [Load CSV data](https://www.tensorflow.org/tutorials/load_data/csv) script that we prepared during today's class.  Following the *Mixed data types* section from the exercise, replace the titanic dataset first with the **Metro Interstate Traffic Volume Data Set** and then with the **Iris Dataset**.  You can use the `read_csv()` command from the pandas package to pull these datasets from the following web addresses.

- https://archive.ics.uci.edu/ml/machine-learning-databases/00492/Metro_Interstate_Traffic_Volume.csv.gz
- https://storage.googleapis.com/download.tensorflow.org/data/iris_training.csv

Use the `plot_model()` command from `tf.keras.utils` to produce the plot that describes the input preprocessing step.  Describe the plot of each model for the two dataset preprocessing steps.  What does each box in the illustration represent?  Are there different paths towards the final concatenation step?  What is occurring at each step and why is it necessary to execute before fitting your model.  Train each model and produce the output (not necessary to validate or test).  Describe the model output from both the  metro traffic interstate dataset and the iris flowers dataset.  What is the target for each dataset?  How would you assess the accuracy of each model?  Are you using a different metric for each one?  Why is this so?  What is each one measuring?

### For tomorrow, read and produce the script on [Custom training: walkthrough](https://www.tensorflow.org/tutorials/customization/custom_training_walkthrough) in preparation for class.









