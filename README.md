# testing_transformations_improve_image_classification
The aim of this project is to test several image transformation techniques that take far
less time compared to CNN embeddings from multiple sources to see if a better score can be
achieved than embedding and a standard SVC. The dataset that will be used is the parakeets
datasets parakeetsNL_with200.zip and the notroseringed_0145977-230530130749713
_200samples.zip (dataset provided from canvas). The results of each transformation will be
evaluated in comparison to the baseline SVC, which uses a gamma value of 0.001. This
assessment is conducted across five random states for data splitting, and the performance
metrics considered are the average accuracy, recall, and F1-score.

methods used:
from color correction :luminance_weighted_Grey_world, Automatic_color_equalization, Retinex_with_adjust
from paper : CLAHE,laplacian operator (the code from the paper's github was not use only the idea to test these algortithms was)
from mt own ideas: The red channel transformation was done with the idea that the main
difference between the two bird species was the rose coloured ring around the bird's neck.
Therefore isolating and only using the red color might allow the model to see the differences
more clearly.The second algorithm mainly increases the contrast of the image in hopes to
display the rose ring more clearly.

more detail and explanation in pdf in repository

Refrences:

color correction package:
Shunsuke Aihara. (n.d.). GitHub - shunsukeaihara/colorcorrect. GitHub.
https://github.com/shunsukeaihara/colorcorrect

paper:
Shen, X., Tian, X., He, A., Sun, S., & Tao, D. (2019b). Transform-Invariant Convolutional neural
networks for image classification and search. arXiv (Cornell University).
https://doi.org/10.48550/arxiv.1912.01447
