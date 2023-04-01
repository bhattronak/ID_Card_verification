# ID Card Verification using Computer Vision
This project is an implementation of ID card verification using computer vision in Python. The program takes an image of an ID card as input and verifies its authenticity by checking if the ID card contains the correct logo and template.

### Requirements: 
Python 3.x
OpenCV
PIL library
Make sure all the required libraries are installed.
Place the ID card image to be verified in the same folder as the code.
Run the Student_id_identifier() function and pass the path of the image as a parameter.

### Functionality:
The Student_id_identifier() function takes an image of an ID card and performs the following tasks:

1. Loads the template images of the logo and the ID card.
2. Performs template matching using normalized correlation coefficient.
3. Checks if the maximum correlation coefficient is above a threshold.
4. Draws a rectangle around the detected logo on the image.
5. Maps other boxes based on the location of the detected logo.
6. Crops the institute logo, candidate photo, and student name from the image.
7. Displays the detected boxes and the cropped images.
8. Checks if the maximum correlation coefficient of the ID card template is above a threshold.
9. Crops the student ID from the image.
10. Displays the result indicating whether the ID card is valid or not.
11. Check that function for various input images such as id card, Institute logo and random image.

### Detailed Explanation of code 
This code is for identifying the student ID in an image. The code uses computer vision techniques to detect a logo and an ID verification template in the image, and then extracts the relevant information from the image.

The code imports the required libraries, which are cv2 for OpenCV and PIL for image processing. It defines a function called Student_id_identifier which takes an image path as input.

The function starts by loading the template images for the logo and the ID verification template. It then loads the input image and gets the width and height of the templates.

The function performs template matching using the normalized correlation coefficient, which is a measure of the similarity between two images. It calculates the correlation coefficient between the input image and the template image at each location in the input image. The result is a matrix of correlation coefficients, which indicates how well the template matches the input image at each location.

The function then finds the location in the input image where the maximum correlation coefficient occurs for both the logo and the ID verification template. If the maximum correlation coefficient is above a threshold value of 0.9 for the logo and 0.98 for the ID verification template, it indicates that the template has been found in the input image.

If the logo is found, the function draws a rectangle around the logo on the input image, and extracts the logo, candidate photo, student name, and student ID from the input image using the location of the logo. The function then displays the extracted images and prints a message indicating that the student has been verified.

If the logo is not found, the function prints a message indicating that the input image is invalid and asks the user to try again.

Here are the steps used in the code to match the templates:

1.Load the template and input images using cv2.imread.
2.Get the width and height of the templates using shape.
3.Perform template matching using cv2.matchTemplate, which returns a matrix of correlation coefficients.
4.Find the location in the input image where the maximum correlation coefficient occurs using cv2.minMaxLoc.
5.Draw a rectangle around the template on the input image using cv2.rectangle.
6.Extract the relevant information from the input image using Image.open and crop.
7.Display the extracted images using display.
8.Print a message indicating the status of the student ID verification.

### Note:
The system assumes that the ID card image has a similar structure and format as the provided templates. Therefore, it may not work accurately for ID cards with different structures or formats.

### Conclusion:
This project is a simple example of how computer vision can be used to verify the authenticity of ID cards. The system can be further improved by implementing machine learning algorithms for better accuracy and robustness.




