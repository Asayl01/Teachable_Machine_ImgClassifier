# Teachable Machine Image Classifier

## Project Description  
This is a simple image classification project to recognize different types of drones — including fixed-wing, fixed-wing VTOL, multi-rotor, and single-rotor helicopter drones — using a machine learning model trained with Teachable Machine.

## Tools Used  
- **Teachable Machine** for training the image recognition model.  
- **TensorFlow / Keras** to export and run the model in Python.  
- **Google Colab** for testing and running the classification script.

##  What is Teachable Machine?  
[Teachable Machine](https://teachablemachine.withgoogle.com/) is a web-based tool by Google that lets you train machine learning models without writing any code.  
tutorial here: [Tutorial Video](https://www.youtube.com/watch?v=kPzEzrc5TcI)

## Testing the Model with Google Colab
Google Colab is a free cloud-based platform by Google that allows users to write and run Python code in a browser.

### How the model was tested
After training the model in Teachable Machine, I exported it in TensorFlow → Keras format, which provided two files:
- keras_model.h5
- labels.txt
- 
Then, I copied the sample Python code provided by Teachable Machine, and pasted it into a new Google Colab notebook.
After minor adjustments (like specifying the input image), the script was able to classify test images based on the trained model.

### Issues Faced  
- Error loading `keras_model.h5` in Google Colab — usually caused by TensorFlow version mismatch.  
  To fix it, run the following command at the start of your notebook:

```python
!pip install tensorflow==2.12.1


