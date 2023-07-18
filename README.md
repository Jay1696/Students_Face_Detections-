# Students_Face_Detections-
  Creating a attendance management system, Our main objective for this system is to extract high-quality features from faces. To accomplish this, we are using a FaceNet system, also known as face embeddings. FaceNet can train a face identification system and an SVM classifier to identify people from photographs.
Introduction
Face recognition is a computer visualization task that recognizes people based on facial photos. FaceNet is a face identification system coded by Google researchers in 2015. The system has accomplished the most advanced results in a run of face recognition data sets. The FaceNet model can be used to extract high-quality features from faces, called face embedding, which can be used to train facial recognition systems. 
Dataset
The dataset we created is of images of students of our class with their consent. Initially, we collected the pictures and then sorted them into folders with the name of the person. There are approximately five to ten images for each person.

 

# Face Recognization Model
  We imported the essential libraries for building the face recognization model. The file name is saved by the name of  "facenet_keras.h5". We used the load_model () function to load the model directly into Keras. Run the example to load the model and print the shape of the input and output tensors. We can see that the model guesses a square colour image as input, with a body of 160 × 160, and will generate a face key as a 128-element vector. We need some additional features for this implementation, but before we send the face image to FaceNet, we need to extract the face from the image.
Now, we will load the dataset and extract the face from each image.  We are loading the dataset to the model and splitting the dataset into the train and test data (trainx, trainy and testx, testy ) as seen.
This will be the outcome of the code, where we can see the loaded images for each class with the name.

  We can see that there is a training data set and a validation or test data set. Watching at some of the photos in the catalogue, we can see that these photos show faces in various directions, light, and sizes.
The important thing is that every image contains a person's face. We will use this data set as the basis of our classifier. We will only train on the "train" data set and classify faces on the "Test" data set. We will advance the face detection system to identify specific faces. The model will use a "data set" for training and testing, which contains five different images of photos of many students. We will use the MTCNN model to search for faces. The FaceNet model will be used to create face mosaics for each different file. Then, we will create a linear support vector machine (SVM) classifier model to predict the value of a given face.
The data set is ready to be input into the face detection model.  Create the face mosaic  The next step is to create the face mosaic. The key to the face is a vector representing the features extracted from the image. Then it will be compared with vectors generated for other looks. For example, another close vector (to some extent) may be the same person, while another vector that is far away (to some time) may be a different person.  The classifier model that we are going to develop takes face embedding as input and predicts the identity of the face. The FaceNet model will generate this inlay for a given face image. 


# Perform face classification 
  The FaceNet model can be used as a portion of the classifier itself, or we can use the FaceNet model to preprocess faces to produce a face integration that can be kept and used as input for our classifier model. The latter method is preferred because the FaceNet model is large and slow and cannot create facial inlays.  So we can pre-calculate the face embeddings of all faces in training and put them in our
Then we can fit a model. When processing normalized facial key input, a linear support vector machine (SVM) is usually used. This is because the technique is very effective in separating the key vectors of the face. Using the SVC class in sci-kit, learn and setting the `kernel` attribute to `linear.` We may also need probability when we make predictions later, which can be set by setting `probability` to `True.`

We plotted one image randomly to see how our model performs. 

# Conclusion
  Deep neural networks work better than machine learning models in terms of extracting meaningful features. Although, the limitation of this network is the requirement of a large amount of data. We try to manage this issue with the aid of a pre-trained model. The pre-trained model is a model that has been trained as a large dataset to gain knowledge about encoding face images. SVM fine-tuning also helps us a lot to push our accuracy to its best outcome. 
Future enhancements 
A facial recognition system can further improvise by including age prediction, emotion prediction, and identification of different face-related health problems. The utilization of facial recognition systems can occur for other purposes rather than a security system.
 
# References
T, J. (2020, November 3). Face Recognition Walkthrough--FaceNet. Pluralsight. https://www.pluralsight.com/guides/face-recognition-walkthrough-facenet
Kaspersky. (2021b, August 9). What is Facial Recognition – Definition and Explanation. Kaspersky Cyber Security Solutions for Home & Business. https://www.kaspersky.com/resource-center/definitions/what-is-facial-recognition
