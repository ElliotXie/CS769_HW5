Install Python 3.8.1, and download the dataset using the link https://drive.google.com/drive/folders/1e1WQLA2Yh_r7bFeqmen3TxtXW7nICZrY?usp=sharing

Please create a folder named "data" and then put the downloaded files into the folder.

This part focuses on enhancing the main model. Significant improvements and extensions have been applied to the performer_pytorch.py file. Below is a structured guide on how to utilize these enhancements and a summary of the key changes:


Running the Enhanced Model:

To observe the impact of these extensions, please follow the code and instructions outlined in the Major Fine-Tune section.
To explore the effect of different modules, directly run the first three modules to get the result of initial learning rate and shared cross layer parameters.
After getting prediction using fine-tuned models (pre train untouched), run module 4 and 5 for further model improvement comparison results
Final module is not implementable but rather demonstrates the triple loss we tried.


Summary of Changes and Modules:

Second Module: Introduction of a mechanism for setting the initial learning rate and tuning shared cross-layer parameters.
Third Module: Implementation of methodologies from the original paper.
Fourth Module: Integration of knowledge distillation techniques.
Fifth Module: Enhancement with hyperparameter tuning in CosineAnnealingWarmupRestarts.
Final Module: Deployment of triple loss testing, allowing for more robust evaluation of the model's performance.

