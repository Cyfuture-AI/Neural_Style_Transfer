🎨 Neural Style Transfer : 
This project implements the neural style transfer technique using TensorFlow. It takes a content image and a style image and blends them to create an output image that retains the content of the first image but adopts the artistic style of the second.

📝 Description :
Neural style transfer is an optimization technique that merges two images—a content image and a style reference image (like an artwork by a famous painter). The goal is to generate a new image that looks like the content image, but “painted” in the style of the style reference image.

This is achieved by optimizing the output image to match both the content statistics of the content image and the style statistics of the style reference image. A convolutional neural network is used to extract these statistics.

✨ Example :
For instance, if we take a content image of a dog and a style image of Wassily Kandinsky's "Composition 7," the algorithm can produce an image of the dog as if it were painted by Kandinsky.

Content Image + Style Image = Stylized Output

💻 Requirements :
This project uses the following Python libraries:

TensorFlow

NumPy

Matplotlib

Pillow (PIL.Image)

IPython.display (for Jupyter notebooks)

functools

time

🚀 Usage :
To run this project, follow the steps in the provided Jupyter notebook (neural_style_transfer.ipynb):

Import Libraries: Run the first cell to import all the necessary libraries and configurations.

Set Image Paths: In the second code cell, update the content_path and style_path variables with the correct local file paths for your content and style images.

Execute the Notebook: Run the remaining cells in order. The notebook will:

Preprocess and resize the images.

Load a pre-trained model from TensorFlow Hub for feature extraction.

Define content and style loss functions.

Run an optimization loop to generate the stylized image.

🔑 Key Functions :
load_img(path_to_img): Reads and preprocesses an image file. It decodes the image, normalizes pixel values, resizes it to a maximum dimension of 512 pixels while maintaining the aspect ratio, and adds a batch dimension.

imshow(image, title=None): Displays an image tensor using Matplotlib, removing the batch dimension if present.
