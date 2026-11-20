# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION-Completion-requirements

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Algorithm

### Step 1: Import Libraries

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2: Create a Blank Image

Create a blank image of size 500 × 500 using NumPy.

### Step 3: Insert Text

Insert the text "Hello World" onto the blank image using OpenCV's `cv2.putText()` function.

### Step 4: Display the Input Image

Display the original image containing the text.

### Step 5: Create a Kernel

Create a 3 × 3 square structuring element using NumPy.

### Step 6: Image Erosion

- Apply erosion using `cv2.erode()`.
- Shrink the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply dilation using `cv2.dilate()`.
- Expand the boundaries of foreground objects.
- Display the dilated image.

### Step 8: Compare the Results

Compare the original, eroded, and dilated images.

## Program
## Developed By
- **Name:** MADHUMITHA R R
- **Register No:** 212224240083
  
### Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
import numpy as np
```

### Step 2: Create a Blank Image

```python
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

### Step 3: Insert Text on the Image

```python
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

### Step 4: Display the Input Image

```python
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
```

### Step 5: Create a Kernel

```python
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```

### Step 6: Apply Erosion

```python
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
```

### Step 7: Display the Eroded Image

```python
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```

### Step 8: Apply Dilation

```python
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
```

### Step 9: Display the Dilated Image

```python
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
```

## Output

### 1. Original Image

<img width="263" height="311" alt="image" src="https://github.com/user-attachments/assets/46cac687-9873-4f8a-8621-b1e8353663a1" />


### 2. Erosion

<img width="260" height="305" alt="image" src="https://github.com/user-attachments/assets/4a26ede9-01f2-4f41-8e24-0f61efe5ec43" />


### 3. Dilation

<img width="437" height="485" alt="image" src="https://github.com/user-attachments/assets/266b5d71-9be2-423e-8022-42c79f78bd34" />


## Result

Thus, the morphological operations **Erosion and Dilation** were successfully implemented using OpenCV.

