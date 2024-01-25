# Image-Blending-using-Laplacian-Pyramid-in-OpenCV-Python
This Python script demonstrates the process of blending two images using the Laplacian pyramid technique in OpenCV. The code takes two input images, "fruit.jpg" and "java.jpg," and creates a visually appealing blend of the two images by combining their Laplacian pyramids.
Dependencies
Make sure you have the following dependencies installed:

OpenCV
NumPy
Install them using the following:
pip install opencv-python numpy

Usage
Place the input images, "fruit.jpg" and "java.jpg," in the same directory as the script.

Run the script:
python image_blending.py

The script will generate a blended image named "fruit_apple.jpg" in the same directory.

The blended image will also be displayed using OpenCV.

Code Overview
Loading Images: The script loads two input images, "fruit.jpg" and "java.jpg," and horizontally concatenates them.

Gaussian Pyramid: Gaussian pyramids are constructed for both images using the cv2.pyrDown function to create a multi-scale representation.

Laplacian Pyramid: Laplacian pyramids are then created for both images by taking the difference between each level of the Gaussian pyramid and the expanded version of the next level.

Blending: The Laplacian images of the two images are blended by horizontally concatenating the left part of the apple Laplacian and the right part of the orange Laplacian at each level.

Reconstruction: The script reconstructs the blended image by iteratively applying the cv2.pyrUp function to the top level of the Laplacian pyramid and adding the corresponding level of the blended Laplacian pyramid.

Saving and Display: The final blended image is saved as "fruit_apple.jpg," and the result is displayed using cv2.imshow.


License
This script is provided under the MIT License. Feel free to modify and use it according to your needs.

Acknowledgments
This code is based on the concept of Laplacian pyramid blending in image processing. Special thanks to the OpenCV and NumPy communities for their valuable contributions.

Please note that the script assumes the input images are in the same directory as the script. Adjust the file paths accordingly if your images are located in a different directory.
