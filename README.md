# computer-vision
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Read an image from file
image_path = 'path/to/your/image.jpg'
img = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

# Apply Canny edge detection
edges = cv2.Canny(img, 50, 150)

# Display the original and edge-detected images using matplotlib
plt.subplot(121), plt.imshow(img, cmap='gray'), plt.title('Original Image')
plt.subplot(122), plt.imshow(edges, cmap='gray'), plt.title('Edge Detection')
plt.show()
