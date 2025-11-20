<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"><html><head></head><body>





<hr/>
<h1>Introduction</h1>
<p>Welcome to our repository dedicated to the fine tuning of Stable Diffusion, an open source neural network for the generation of high quality images. The aim of this project is to improve the capabilities of Stable Diffusion by fine-tuning it with datasets from the gaming industry.

Stable Diffusion is a deep learning model that generates images from text, and it was released in 2022 based on diffusion techniques. The model is mainly utilised for producing detailed images based on textual descriptions, but it can also be employed for other tasks, such as inpainting, outpainting, and generating image-to-image translations guided by a text prompt (Wikipedia contributors, 2024).</p>

<hr/>
<h1>Getting Started</h1>
<h2>Prerequisites</h2>
<ul>
  <li>Python 3.9+</li>
  <li>Installing the dependencies listed in requirements.txt.</li>
</ul>
<code>
  pip install -r requirements.txt
</code>

<h1>Data Preparation</h1>
<p>To prepare your data for fine-tuning the Stable Diffusion model, follow these steps:</p>
<h2>Step 1: Organize The Image Dataset</h2>
<p>Place all the images you wish to use for fine-tuning inside the <code>
./data/images/
</code> folder.</p>
<h2>Step 2: Write Prompt for Images</h2>
<ul>
  <li>In Dreambooth, fine-tuning of all images is done using only one well-defined prompt.</li>
  <li>Multiple Prompt (for Keras-CV): <br/> A separate prompt for each image in the dataset is required to implement stable diffusion with Keras-CV. The BLIP model can be used with the <code> ./preparation/auto prompting using the BLIP.ipynb </code> script to automatically generate descriptive captions for each image in the dataset.</li>
</ul>

<h1>Fine-Tuning Process</h1>
<h2>Using Dreambooth</h2>
<p>In this approach, the Stable Diffusion model got fine-tuned using Dreambooth. It involves setting up the model from huggingface and fine-tuning it with given gaming characters. The fine-tuned model then is used to generate new artwork related to gaming characters.</p>
<h2>Using Keras-CV</h2>
<p>In this appraoch, the Stable Diffusion model got fine-tuned using TensorFlow&#39;s Keras framework. A custom class is used for handling the training processes (including loss calculation and gradient updates) which updates part of the weight of the the diffusion model.</p>
<h2>Evaluation</h2>
<p>The fine-tuned stable diffusion model has generated a set of character images for evaluation. The images confirm the model&#39;s ability to:
<ul>
	<li>Presence of Requested Object: Each image clearly displays the intended fantasy characters.</li>
 <li>Variation in Design: There&#39;s evident variation among characters, with differences in shapes and colors showcased.</li>
 <li>Background Simplicity: Characters are set against solid, non-complex backgrounds for clarity.</li>
 <li>Separation from Background: The subjects are well-differentiated from the backdrop, ensuring easy discernibility.</li>
</ul></p>
<h2>Character Variation</h2>
<p><img src="./generated artworks/dreambooth/Gandalf the gray.png" alt="Gandalf the gray" style="width:150px;height:150px;"/>
Gandalf the gray.</p>
<p><img src="./generated artworks/dreambooth/Elfs with arrows.png" alt="Elfs with arrows" style="width:150px;height:150px;"/>
Elfs with arrows</p>
<p><img src="./generated artworks/dreambooth/a knight in purple, black and white with an elaborate helmet on his head.png" alt="a knight in purple, black and white with an elaborate helmet on his head" style="width:150px;height:150px;"/>
a knight in purple, black and white with an elaborate helmet on his head.</p>
<p><img src="./generated artworks/dreambooth/a demon dressed in red and holding a sword.png" alt="a demon dressed in red and holding a sword" style="width:150px;height:150px;"/>
a demon dressed in red and holding a sword.</p>

<h2>Colour Variation of Same Characters</h2>
<p><img src="./generated artworks/dreambooth/Knights in blue, black and white with an elaborate helmet on their head.png" alt="Knights in blue, black and white with an elaborate helmet on their head" style="width:150px;height:150px;"/>
Knights in blue, black and white with an elaborate helmet on their head.</p>
<p><img src="./generated artworks/dreambooth/Knights in green, black and white with an elaborate helmet on their head.png" alt="Knights in green, black and white with an elaborate helmet on their head" style="width:150px;height:150px;"/>
Knights in green, black and white with an elaborate helmet on their head.</p>
<p><img src="./generated artworks/dreambooth/Knights in red, black and white with an elaborate helmet on their head.png" alt="Knights in red, black and white with an elaborate helmet on their head" style="width:150px;height:150px;"/>
Knights in red, black and white with an elaborate helmet on their head.</p>
</body>
</html>