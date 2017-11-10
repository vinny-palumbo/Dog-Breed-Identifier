[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Dog Output"
[image2]: ./images/sample_human_output.png "Sample Human Output"

# Dog Breed Identifier

In this project, I've built a pipeline that can be used within a web or mobile app to process real-world, user-supplied images.  Given an image of a dog, the algorithm identifies an estimate of the canine’s breed.  If supplied an image of a human, the algorithm identifies the resembling dog breed.  

![Sample Dog Output][image1]

![Sample Human Output][image2]

### Datasets

1. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 
2. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  

### Environment

Obtain the necessary Python packages, and switch Keras backend to Tensorflow.  
	
	For __Mac/OSX__:
	```
		conda env create -f requirements/aind-dog-mac.yml
		source activate aind-dog
		KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```

	For __Linux__:
	```
		conda env create -f requirements/aind-dog-linux.yml
		source activate aind-dog
		KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```

	For __Windows__:
	```
		conda env create -f requirements/aind-dog-windows.yml
		activate aind-dog
		set KERAS_BACKEND=tensorflow
		python -c "from keras import backend"
	```

## Possible Future Improvements:

#### Implement the Algorithm into a Web App

Implement the algorithm into a web app using [Flask](http://flask.pocoo.org/) or [web.py](http://webpy.org/docs/0.3/tutorial)!  

#### Overlay Dog Ears on Detected Human Heads

Overlay a Snapchat-like filter with dog ears on detected human heads.  Determine where to place the ears through the use of the OpenCV face detector, which returns a bounding box for the face.  To also overlay a dog nose filter, some nice tutorials for facial keypoints detection exist [here](https://www.kaggle.com/c/facial-keypoints-detection/details/deep-learning-tutorial).

#### Add Functionality for Dog Mutts

Currently, if a dog appears 51% German Shephard and 49% poodle, only the German Shephard breed is returned.  The algorithm is currently guaranteed to fail for every mixed breed dog.  Of course, if a dog is predicted as 99.5% Labrador, it is still worthwhile to round this to 100% and return a single breed.

#### Experiment with Multiple Dog/Human Detectors

Perform a systematic evaluation of various methods for detecting humans and dogs in images.  Provide improved methodology for the `face_detector` and `dog_detector` functions.
