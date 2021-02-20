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
		- Convolve the 3x3 filter over the 9x9 matrix and provide the resulting matrix. ![alt text](https://github.com/tyler-frazier/applied_machine_learning/blob/master/dailies/cnn_xtra_q.png)  

- Friday:
	- Module 1.2


## Week 5 (2/22)
- Monday:
	- Module 1.3
- Wednesday:
	- Module 1.3
- Friday:
	- Project 1

## Week 6 (3/1)
- Monday:
	- Module 2.1
- Wednesday:
	- Module 2.1
- Friday: Post Spring Break Day, Open Session / Workshop (3/5)

## Week 7 (3/8)
- Monday:
	- Module 2.2
- Wednesday:
	- Module 2.2
- Friday:
	- Module 2.2

## Week 8 (3/15)
- Monday:
	- Module 2.3
- Wednesday: Spring Break Day, No Class (3/17)
- Friday:
	- Project 2

## Week 9 (3/22)
- Monday:
	- Module 3.1
- Wednesday:
	- Module 3.1
- Friday:
	- Module 3.1

## Week 10 (3/29)
- Monday:
	- Module 3.2
- Wednesday:
	- Module 3.2
- Friday:
	- Module 3.2

## Week 11 (4/5)
- Monday:
	- Module 3.3
- Wednesday: Spring Break Day, No Class (4/7)
- Friday:
	- Project 3

## Week 12 (4/12)
- Monday:
	- Module 4.1
- Wednesday:
	- Module 4.1
- Friday:
	- Module 4.1

## Week 13 (4/19)
- Monday:
	- Module 4.2
- Wednesday:
	- Module 4.2
- Friday:
	- Module 4.2

## Week 14 (4/26)
- Monday: Spring Break Day, No Class
- Wednesday:
	- Module 4.3
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
