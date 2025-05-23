# IITISOC-24-ML-23
<h1>Team details: </h1>

<b>Team leader<b>: Kshithij Singhania <br>
<b>Roll no.<b>: 230002035   <br>
<b>email id<b>: ee230002035@iiti.ac.in   <br>

<b>Team member 1<b>: Prateek   <br>
<b>Roll no.<b>: 230002057     <br>
<b>email id<b>: ee230002057@iiti.ac.in   <br>



<p><h1>Multilingual OCR with EasyOCR and Hugging Face Transformers</h1>
<h2>About</h2>
Welcome to the Multilingual OCR repository! This project leverages the power of EasyOCR, a comprehensive and easy-to-use Optical Character Recognition (OCR) library, to extract text from images in multiple languages. Additionally, it integrates a translation transformer model from Hugging Face to translate the extracted text into various languages. Furthermore, this repository includes a custom-trained English OCR model for specialized text recognition tasks.

<h2>Key Features</h2>
EasyOCR Integration: Utilize pre-trained models from EasyOCR to recognize text from images in over 6 languages.
Custom English OCR Model: Includes a custom-trained model specifically for recognizing English text, with dedicated training and testing files.
Translation Transformer: Translate the extracted text into different languages using state-of-the-art transformer models from Hugging Face.
Multilingual Support: Handle a variety of languages for both OCR and translation tasks.
Ease of Use: Simple and straightforward implementation, making it accessible for developers of all levels.
## Components
EasyOCR: An OCR library that provides pre-trained models capable of recognizing text in multiple languages with high accuracy.
Custom English OCR Model: A specialized model trained for English text recognition, which first crops images into words before making predictions.
Training File: Contains the code and data for training the custom English OCR model.
Testing File: Provides a custom testing setup for evaluating the performance of the trained model.
Hugging Face Transformers: A collection of transformer models for translation tasks, allowing for seamless language translation of the recognized text.
## Applications
Document Digitization: Convert printed or handwritten text in different languages into digital text.
Language Translation: Translate recognized text into various languages for multilingual support.
Data Extraction: Extract and translate text from images for data analysis and processing..</p>

## Technologies Used

- **OCR**: [EasyOCR](https://github.com/JaidedAI/EasyOCR) for text extraction.
- **Translation**: [Hugging Face Transformers](https://github.com/huggingface/transformers) for text translation.
- **Web Interface**: [Gradio](https://gradio.app/) for building the web interface.
- **Image Processing**: [OpenCV](https://opencv.org/) for handling image files.

  <h1>Installation of multilingual ocr</h1>
<p> For the pretrained model ocr we just have to run the [Multilingual_OCR(1).ipynb] file : <br>(https://github.com/Pradeep-Kumar-Rebbavarapu/IITISOC-24-ML-23/blob/main/MultiLingual_OCR%20(1).ipynb) file. </p>
<p>Download Image1, Image2, Image3 for example used on interface </p>


  <h1>Installation of English ocr model</h1>
  <p> For our own trained english only ocr :</p><br>
To check training part run OCR_Training.ipynb <br>
This training file is trained with a famous dataset IAM dataset which is a dataset constituent of handwritten chracters with there specific labels and a word.txt file which has a specific greyscale which played amajor role in training <br>
initially we need to copy the desired image path into Input image section in main.py file<br>
main.py along with __init__.py popularises the test image using certain kernel,gray scales,sigma,theta and image height(should be changed according to input image) arguments.This main.py finally detects the popularlised words and creates a box around it,croping indivisual words and saving it into Outputs2 folder<br>
<p>
<img src="image4.png">
</p>
<h2>Algorithm</h2>
The illustration below shows how the algorithm works:

<li>top left: input image</li>
<li>top right: apply filter to the image</li>
<li>bottom left: threshold filtered image</li>
<li>bottom right: compute bounding boxes</li>
<img src="imgae5.jpg">
<p>The filter kernel with size=25, sigma=5 and theta=3 is shown below on the left. It models the typical shape of a word, with the width larger than the height (in this case by a factor of 3). On the right the frequency response is shown (DFT of size 100x100). The filter is in fact a low-pass, with different cut-off frequencies in x and y direction.</p>
<img src="image6.jpg">
<h3>Training model</h3>
<p>
Training model is difficult to explain here in text for us , the model contains Convo 2D layer and a ctc loss function which makes it unique
<br>
will be sharing the detailed explanation in the presentation <b>:) </b> 
</p>


