# ID Card Verification using Computer Vision
This project is an implementation of ID card verification using computer vision in Python. The program takes an image of an ID card as input and verifies its authenticity by checking if the ID card contains the correct logo and template.

###Requirements: 
Python 3.x
OpenCV
PIL library
How to use
Clone the repository to your local machine.
Make sure all the required libraries are installed.
Place the ID card image to be verified in the same folder as the code.
Run the Student_id_identifier() function and pass the path of the image as a parameter.

### Functionality:
The Student_id_identifier() function takes an image of an ID card and performs the following tasks:

Loads the template images of the logo and the ID card
Performs template matching using normalized correlation coefficient
Checks if the maximum correlation coefficient is above a threshold
Draws a rectangle around the detected logo on the image
Maps other boxes based on the location of the detected logo
Crops the institute logo, candidate photo, and student name from the image
Displays the detected boxes and the cropped images
Checks if the maximum correlation coefficient of the ID card template is above a threshold
Crops the student ID from the image
Displays the result indicating whether the ID card is valid or not.

### Note:
The system assumes that the ID card image has a similar structure and format as the provided templates. Therefore, it may not work accurately for ID cards with different structures or formats.

### Conclusion:
This project is a simple example of how computer vision can be used to verify the authenticity of ID cards. The system can be further improved by implementing machine learning algorithms for better accuracy and robustness.




