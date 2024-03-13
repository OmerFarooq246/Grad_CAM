<h1>Grad_CAM</h1>
<h6>2nd Project - NCAI, DLL internship</h6>


<p>The rise of convolutional Neural Network has proven to be a break through in machine learning, enabling deep nerual networks to provide excellent performance in various vision related tasks varying from image classification to visual question answering. But with this benefit comes a drawback that as the deep NNs have become intricate, they have also become more harder to interpret.</p>

<hr>

Explainable AI is an approach that allows developers and users to understand the behaviour of different neural networks. One of the techniques of explainable AI is Grad_CAM (Gradient Weighted Class Activation Mapping).

Grad_cam is a rough localized map that highlights the areas of an image that are important for the model in predicting a certain target class. It uses the gradients of any target class flowing into the final convolutional layer to produce a localization map.

Following are the steps for generating a Grad_CAM:
  1. Derivative of the raw score of the interested class with respect to the last convolutional output.
  2. Global average pooling of the derivative to get the "importance weights": a 1-D vector.
  3. Linear combination of importance weights with the last conv output.
  4. Applying ReLU or Normalizing the output between 0 and 1.
  5. Superimposing the heatmap and the original image.

<h4>Diagram:</h4>
<img width=850 src="https://github.com/OmerFarooq246/Grad_CAM/assets/110720771/2faf34b8-b86e-4fbe-9d3d-5dcaa6fd04ea">

<h4>Results:</h4>
<p>(Input,   w.r.t Cat,   w.r.t Dog)</p>
<img width=350 src="https://github.com/OmerFarooq246/Grad_CAM/assets/110720771/9c4e05c9-7633-4ac7-8936-da2883363db2">
<img width=300 src="https://github.com/OmerFarooq246/Grad_CAM/assets/110720771/977bf02e-9c86-4a7d-b3c5-d095df307b73">
<img width=300 src="https://github.com/OmerFarooq246/Grad_CAM/assets/110720771/395f4292-8ef6-4f11-abba-f5fe0b166512">
<br>
<br>
The model is deployed on Huggin Face: https://huggingface.co/spaces/OmerFarooq/Grad_cam

<h4>Original Paper Link:</h4>
<a href="https://arxiv.org/abs/1610.02391">Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization.</a>
