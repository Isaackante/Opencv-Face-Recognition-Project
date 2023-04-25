# Face Recognition using Local Binary Patterns Histograms (LBPH)

This code implements face recognition using the LBPH algorithm in OpenCV. The LBPH algorithm extracts local binary patterns from the images and constructs histograms for each face. These histograms are used to train a machine learning model that can then recognize faces in real-time.

# Code Explanation
The code consists of four main functions:

1. faceSampling()
This function is used to capture face images and store them in a dataset folder. It uses the Haar Cascade classifier to detect faces in real-time video, and captures 80 images for each person's face. The images are saved in the dataset folder with a unique filename based on the person's name and the count of images captured.

2. faceLearning()
This function reads the face images from the dataset folder and trains the LBPH model. It uses the Haar Cascade classifier to detect faces in the images, and extracts the local binary patterns from each face to construct a histogram. The histograms are used to train the LBPH model, which is saved to the trainerdata.yml file.

3. faceRecognition()
This function uses the trained LBPH model to recognize faces in real-time video. It uses the Haar Cascade classifier to detect faces in the video, and extracts the local binary patterns from each face to construct a histogram. The histograms are then compared to the trained LBPH model to determine the identity of the person.

4. main()
This function is the main entry point for the program. It calls the faceSampling(), faceLearning(), and faceRecognition() functions in sequence to capture face images, train the LBPH model, and recognize faces in real-time video.
