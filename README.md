# Sports-Persons-Classifier-
**Working:**
- Image we give to the UI gets sent to the back end that is the flask server where our function "classify_image" uses our saved ML pickle model from artifacts folder.
- Model trained using Support Vector Classifier.
- Image changed to a base 64 encoded string and then the base64 encoded string is converted into a cv2 image using numpy and cv2's imdecode function.
- Now the cv2 image can be easily used to run the haar cascade module of openCV to detect face and eyes.
- If the image has a clear face with a set of 2 eyes, we generate a cropped image of the face which is our region of interest.
- We will use cropped image and apply wavelet transform to extract meaning features that can help with image identification.
- The wavelet transform image and raw pixel image is vertically stacked and the combined image is used to  classify the image.

**Future Scope/ Way Forward:**
- use deep learning algorithms like CNN or GAN for better accuracy
- Increase the dataset toy improve the usability of the model.
- Improve the UI
- Host/Deploy on Heroku or other online platforms
