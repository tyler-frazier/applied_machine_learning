# Semester Schedule

## Week 1 (1/27)
- Wednesday:
	- Introductions
		- Zoom, Slack, Blackboard & the Syllabus
	- For next time:
		- [Getting Started with GitHub, Markdown & Webstorm](https://tyler-frazier.github.io/dsbook/gitstart.html)
- Friday:
	- Using GitHub & Markdown
	- For next time:
		- [Installing Python & Pycharm](https://tyler-frazier.github.io/dsbook/pyinstall.html)

## Week 2 (2/1)
- Monday:
	- Using PyCharm
		- [Getting Started with Python & PyCharm](https://tyler-frazier.github.io/dsbook/pystart.html)
	- For next time:
	  	- Lecture 1 - [What is ML by Laurence Maroney](https://www.youtube.com/watch?v=_Z9TRANg4c0)
- Wednesday:
  	- Using PyCharm
		- [Getting Started with Python & PyCharm](https://tyler-frazier.github.io/dsbook/pystart.html)
  	- For next time:
  		- Response (Upload your response to your, public facing, GitHub pages site.
  			- In Laurence Maroney’s video, What is ML, he compares traditional programming with machine learning and argues that the main difference between the two is a reorientation of the rules, data and answers. According to Maroney, what is the difference between traditional programming and machine learning? 
  			- With the first basic script that Maroney used to predict a value output from the model he estimated (he initially started with 10 that predicted ~31. Modify the predict function to produce the output for the value 7. Do this twice and provide both answers. Are they the same? Are they different? Why is this so?
  			- Using the script you produced to predict housing price, take the provided six houses from Mathews, Virginia and train a neural net model that estimates the relationship between them. Based on this model, which of the six homes present a good deal? Which one is the worst deal? Justify your answer.
  			- [Six homes in Mathews download](https://github.com/tyler-frazier/applied_machine_learning/raw/master/dailies/Archive.zip)
  		- Lecture 2 - [First Steps in Computer Vision by Laurence Maroney](https://www.youtube.com/watch?v=j-35y1M9rRU)
- Friday: add/drop period ends
	- For next time:
	  	- Response (Upload your response to your, public facing, GitHub pages site).
	  		- In the video, First steps in computer vision, Laurence Maroney introduces us to the Fashion MNIST data set and using it to train a neural network in order to teach a computer “how to see.” One of the first steps towards this goal is splitting the data into two groups, a set of training images and training labels and then also a set of test images and test labels. Why is this done? What is the purpose of splitting the data into a training set and a test set?
	  		- The fashion MNIST example has increased the number of layers in our neural network from 1 in the past example, now to 3. The last two are .Dense layers that have activation arguments using the relu and softmax functions. What is the purpose of each of these functions. Also, why are there 10 neurons in the third and last layer in the neural network.
	  		- In the past example we used the optimizer and loss function, while in this one we are using the function adam in the optimizer argument and sparse_categorical- crossentropy for the loss argument. How do the optimizer and loss functions operate to produce model parameters (estimates) within the model.compile() function?
	  		- Using the mnist drawings dataset (the dataset with the hand written numbers with corresponding labels) answer the following questions.
	  			- What is the shape of the images training set (how many and the dimension of
   each)?
	  			- What is the length of the labels training set?
	  			- What is the shape of the images test set?
	   			- Estimate a probability model and apply it to the test set in order to produce the array of probabilities that a randomly selected image is each of the possible numeric outcomes (look towards the end of the basic image classification exercises for how to do this — you can apply the same method applied to the Fashion MNIST dataset but now apply it to the hand written letters MNIST dataset).
			- Use np.argmax() with your predictions object to return the numeral with the highest probability from the test labels dataset.
	  		- Produce a plot of your selected image and the accompanying histogram that illustrates the probability of that image being the selected number

## Week 3 (2/8)
- Monday:
	- review fashion_mnist and mnist responses nn
- Wednesday:
	- workshop
	- Stretch Goal: Mini-Project 1 (due date, Sunday midnight)
		- Create a new project folder and setup it up to use the 3.9.1 python interpreter
		- Download these [files](https://github.com/tyler-frazier/applied_machine_learning/raw/master/dailies/miniprj.zip)
		- Also download the [yolov3.weights](https://pjreddie.com/media/files/yolov3.weights)
		- Create and name three new folders in your new project folder, and add the following files.
			- yolo-coco: `coco.names`, `yolov3.cfg`, `yolov3.weights`
			- videos: `rockstar.mp4`
			- output-videos: leave empty for now
		- Install the needed packages (use opencv-contrib-python for cv2)
		- Modify the script `soc_dis_det.py` as needed and run it on the included `.mp4` file
		- Choose your own `.mp4` file and use it instead of the included video to execute the script.
		- Upload your output to GitHub (or include a link to YouTube), create a link to a new Page and answer the following questions
		  - Was your social distance detector effective at detecting potential violations?  Are you able to describe how the distance detector is applying its calculations of either being safe or noting a violation?
		  - Do you think this approach would be effective for estimating new infections in real time? How would you implement such an approach in response to the COVID-19 pandemic we are currently experiencing?
		  - What limitations or improvements might you include in order to improve your proposed design?
- Friday: Spring Break Day, No Class (2/12)

## Week 4 (2/15)
- Monday:
	- Mini-Project 1
	- For next time:
		- Lecture 3 - [Convolutions and pooling by Laurence Maroney](https://www.youtube.com/watch?v=PCgLmzkRM38)
- Wednesday:
	- For next time (Sunday afternoon):
		- Last time you did an exercise (convolutions and pooling) where you manually applied a 3x3 array as a filter to an image of two people ascending an outdoor staircase.  Modify the existing filter and if needed the associated weight in order to apply your new filters to the image 3 times.  Plot each result, upload them to your response, and describe how each filter transformed the existing image as it convolved through the original array and reduced the object size.  What are you functionally accomplishing as you apply the filter to your original array (see the following snippet for reference)?  Why is the application of a convolving filter to an image useful for computer vision?  Stretch goal: instead of using the misc.ascent() image from scipy, can you apply three filters and weights to your own selected image?  Again describe the results.
		- Another useful method is pooling.  Apply a 2x2 filter to one of your convolved images, and plot the result.  In effect what have you accomplished by applying this filter?  Does there seem to be a logic (i.e. maximizing, averaging or minimizing values?) associated with the pooling filter provided in the example exercise (convolutions & pooling)?  Did the resulting image increase in size or decrease?  Why would this method be useful?  Stretch goal:  again, instead of using misc.ascent(), apply the pooling filter to one of your transformed images.
		- Convolve the 3x3 filter over the 9x9 matrix and provide the resulting matrix. [link to matrices](https://github.com/tyler-frazier/applied_machine_learning/blob/master/dailies/cnn_xtra_q.png)  

- Friday:
	- Review CNNs & Pooling

## Week 5 (2/22)
- Monday:
	- Project 1, due Wednesday, March 3rd by noon
		- Select a city and scrape as many observations as possible from zillow.  Try to obtain at least 400 observations from your selected location.
		- Clean the housing data you obtained and create a number of usable features (independent variables) and targets (dependent variables).  Set price as the response variable, and then set numbers of beds, number of bathrooms and total square footage as the predictors.
		- Following the previous model you specified (6 houses in Mathews), import your new data set and train a new model on your target and features.
		- Write a one and a half to two page report on your results and include the following.
			- A description of the housing data you scraped from zillow
			- A description of your model architecture
			- An analysis of your model output
			- An analysis of the output that assesses and ranks all homes from best to worst deal
		- Include at least three plots that support your project report
		- Stretch goal: add a spatial variable to your feature set and compare with the original model.  Did this improve the predictive power of your model? If so, how?
- Wednesday:
	- Matrix convolutions & mean squared error
	- For next time:
	  	- Convolutions:
			- Convolve the two 3x3 matrices that were assigned to you with your 9x9 matrix and calculate the resulting two matrices
			- What is the purpose of using a 3x3 filter to convolve across a 2D image matrix?
			- Why would we include more than one filter?  How many filters did you assign as part of your architecture when training a model to learn images of numbers from the mnist dataset?
	  	- MSE: From your 400+ observations of homes for sale, calculate the MSE for the following.
	  		- The 10 biggest over-predictions
	  		- The 10 biggest under-predictions
	  		- The 10 most accurate results (use absolute value)
	  		- In which percentile do the 10 most accurate predictions reside? Did your model trend towards over or under predicting home values?
	  		- Which feature appears to be the most significant predictor in the above cases?
	  		- Stretch goal: calculate the MAE and compare with your MSE results  
- Friday:
	- Plotting and interpreting model results

## Week 6 (3/1)
- Monday:
	- Module 2
- Wednesday:
	- Project 1 due
	- For next time:
		- [R warm-up exercise](https://tyler-frazier.github.io/dsbook/rstart.html#creating-a-more-complicated-plot-while-also-creating-and-then-using-a-data-frame)
		- [Create a DHS account](https://dhsprogram.com/data/dataset_admin/login_main.cfm?CFID=20207729&CFTOKEN=12c58a1ece6a16a6-D441CCAC-D284-DBF3-C59B94AD3BD48730)
		- [Select a country](https://dhsprogram.com/data/available-datasets.cfm)
		  	- Standard DHS, Phase V or newer is best
		- [Request DHS data](https://dhsprogram.com/data/dataset_admin/index.cfm?action=createproject)
			- After logging into your account: (1) select a country; (2) write a brief project proposal in order to request access to the DHS survey data (see below) and then also (3) request access to the center points (shapefiles) for each enumeration area.  Following is a draft proposal you are welcome to modify in order to construct your own request.  You are also welcome to include my name as a project co-researcher.
			- Proposal boilerplate: I am in an Applied Machine Learning course at William & Mary, where I am constructing models using various types of development and health related data. This data will be used with machine learning models as the basis to investigate different dimensions of human development in [my selected country]. Using results from this model, I will describe health care, education, migration and wealth within [my selected country].  I am also requested the GPS data from the DHS website to produce accurate geospatial population and development models for [my selected country]. Providing access to the corresponding geospatial information for each survey observation would help improve accuracy over a model based solely on  survey data without coordinates.

- Friday: Post Spring Break Day, Open Session / Workshop (3/5)

## Week 7 (3/8)
- Monday:
	- Request the DHS data
- Wednesday:
	- Data wrangling and analysis
	- For next time:
		- Import the households dataset for your selected country and create a data frame with a variable that describes each of the following.
			- household ID
		  	- unit 
		  	- weights 
		  	- location
		  	- size
			- gender
			- age
			- education
			- wealth
		- Pivot the persons columns within your households data to a long format in order to produce a similarly specified dataset that describes all persons residing within all households.
		- Using this data frame describing all persons standardize, normalize and percentize your variables and visualize each post transformed dataset as a heatmap that illustrates the heterogeneity of the combination of patterns.

- Friday:
	- Module 2.  Logistic regression and random forest models in R with your DHS data

## Week 8 (3/15)
- Monday:
	- Module 2.  Linear estimation, logistic regression and boosted trees estimation models in python with your DHS data
- Wednesday: Spring Break Day, No Class (3/17)
- Thursday:
	- Project 2, due Wednesday, March 24th by midnight
		- Using the R script provided, split and sample your DHS persons data and evaluate the AUC - ROC values you produce.  Which "top_model" performed the best (had the largest AUC)? Are you able to use the feature selection penalty to tune your hyperparameter and remove any potentially irrelevant predictors?  Provide justification for your selected penalty value?  Finally, provide your ROC plots and interpret them.  How effective is your penalized logistic regression model at predicting each of the five wealth outcomes.
		- Using the R script provided, set up your random forest model and produce the AUC - ROC values for the randomly selected predictors, and the minimal node size, again with wealth as the target.  How did your random forest model fare when compared to the penalized logistic regression?  Provide your ROC plots and interpret them.  Are you able to provide a plot that supports the relative importance of each feature's contribution towards the predictive power of your random forest ensemble model?
		- Using the python script provided, train a logistic regression model using the tensorflow estimator API and your DHS data, again with wealth as the target.  Apply the linear classifier to the feature columns and determine the accuracy, AUC and other evaluative metrics towards each of the different wealth outcomes.  Then continue with your linear classifier adding the derived feature columns you have selected in order to extend capturing combinations of correlations (instead of learning on single model weights for each outcome).  Again produce your ROC curves and interpret the results.
		- Using the python script provided, train a gradient boosting model using decision trees with the tensorflow estimator.  Provide evaluative metrics including a measure of accuracy and AUC.  Produce the predicted probabilities plot as well as the ROC curve for each wealth outcome and interpret these results.
		- Analyze all four models.  According to the evaluation metrics, which model produced the best results?  Were there any discrepancies among the five wealth outcomes from your DHS survey dataset?
- Friday:

## Week 9 (3/22)
- Monday:
  	- Fore next time:
  		- Download the administrative subdivision for your selected country. [Download GADM ADMs](https://tyler-frazier.github.io/dsbook/describe.html#projecting-plotting-and-labelling-administrative-subdivisions)
  		- Download the population raster from Worldpop for your selected county following these instructions. [Download population geospatial raster from Worldpop](https://tyler-frazier.github.io/dsbook/describe.html#extracting-populations-from-a-raster-and-aggregating-to-each-unit)
		- Download the 12 rasters from your selected country and stack them following these instructions. [Downloading geospatial rasters from Worldpop](https://tyler-frazier.github.io/dsbook/describe.html#acquiring-modifying-and-describing-the-data)
		- Produce a raster stack and calculate summary statistics using the script posted to our slack channel
- Wednesday:
	- Project 2, due
- Friday:
	- Prep raster stack for Module 3

## Week 10 (3/29)
- Monday:
	- Module 3
- Wednesday:
	- Module 3
- Friday:
	- Module 3

## Week 11 (4/5)
- Monday:
	- Module 3
- Wednesday: Spring Break Day, No Class (4/7)
- Friday:
	- Project 3

## Week 12 (4/12)
- Monday:
	- Module 4
- Wednesday:
	- Module 4
- Friday:
	- Module 4

## Week 13 (4/19)
- Monday:
	- Module 4
- Wednesday:
	- Module 4
- Friday:
	- Module 4

## Week 14 (4/26)
- Monday: Spring Break Day, No Class
- Wednesday:
	- Module 4
- Friday:
	- Project 4

## Week 15 (5/3)
- Monday:
	- Final Project
- Wednesday:
	- Final Project
- Friday: Last day of class
	- Final Project

## Final
- Final Project is due on the last day of the finals period at 5PM.
