# Human-Protien-Atlas

<b>Human Protein Atlas Classification - Featured Competition on Kaggle</b>

The dataset was taken from Kaggle : https://www.kaggle.com/c/dog-breed-identification/data

Problem Statement : Classify subcellular protein patterns in human cells.

<b><h3>Approach :</h3></b>

All samples consist of four files - blue, green, red, and yellow.
<br>All samples are sorted into their respective folder. Each folder of one sample contains the four files.
<br>The train folder is divided into training and validation dataset.
<br>The split between training dataset and validation dataset is 87.5 : 12.5.

The ProteinDataGenerator function is the user defined generator which combines all the filters and converts into one image with 3 filters (A combination of R, G, B, Y).

Data augmentation is applied to training set.
Operations performed :
<ul>
<li>Rescaling</li>
<li>Shearing</li>
<li>Zooming</li>
<li>Rotating</li>
<li>Flipping</li>
</ul>

Transfer learning was applied as dataset was of small size. InceptionV3 network with ImageNet weights was used. The network was trainable.
  
<b><h3>For batch size of 16 and after 500 epochs for image of size 352x352, results are :</h3></b>
<ul>
<li><b>F1 score of 0.345, categorical accuracy of 71.3%</b> on training set.
<li><b>F1 score of 0.310, categorical accuracy of 63.7%</b> on validation set.
<li><b>Loss is 0.053</b> on training set.
<li><b>Loss is 0.065</b> on validation set.
</ul>
