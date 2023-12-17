# CS769HW5

This project is systematically organized into three key components:

Pretraining Phase: The foundational pretraining stage of our project is located in the pretrain folder. Here, you can find all the necessary code and instructions to execute the pretraining part of the project.

Finetuning Phase: For the primary finetuning process, detailed information and code are provided in this section (below). It encompasses the essential steps and guidelines for effectively finetuning our model.

Advanced Finetuning Options: For more advanced and specialized finetuning requirements, please refer to the finetune_extension2 folder. This section offers a diverse range of finetuning options, catering to specific needs and scenarios.

Each part of the project is designed to be standalone yet integrative, ensuring both flexibility and cohesion in the overall workflow.



# Installation
Clone this repository
```
git clone
```
Install Python 3.8.1, and download the below dataset use the link https://drive.google.com/drive/folders/1e1WQLA2Yh_r7bFeqmen3TxtXW7nICZrY?usp=sharing, unzip the data file to root.
- Pretrained model: panglao_pretrain.pth
- Gene embedding: gene2vec_16906.npy
# Datasets
- panglao_10000.h5ad
- Zheng68K.h5ad
- preprocessed_data.h5ad: preprocessed original dataset.
- New_subsampling_300.h5ad: reducing the number of cells to 300.
- New_augmented_4600.h5ad: augmenting the number of BP and MoP to 4600 cells using SMOTE algorithm, function fit_resample and seed=2021.
- New_ranoversampling_4000: augmenting the number of BP and MoP to 4000 cells using RandomOverSampler algorithm, function fit_resample and seed=2021.
# Fine-tune
- new_finetune_percent.py: run scBERT fine-tuning on 10%, 25%, 50%, 75%, and 100% of the training data
- new_finetune.py: used to run fine-tuning (cell type annotation) for scBERT, an example command line call:
  
```
python new_finetune.py --model_name finetune_seed2021 --data_path <path to preprocessed h5ad for fine-tuning> --model_path <path to pre-trained model> --world_size=1 --seed=2021 --epochs=10 --grad_acc=1 --batch_size=32 --pos_embed_g2v
```
# Prediction
Use the model with the best accuracy for prediction. Run the command:
```
python new_predict.py --data_path "new_tests_path.h5ad" --model_path "./ckpts/finetune1_best.pth"
```
