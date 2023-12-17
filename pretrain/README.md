# Pretrain part
python=3.8

# Environment

#pytorch:1.13.1-cuda11.6-cudnn8-devel

!pip install torchvision==0.14.0

!pip install transformers==4.24.0

!pip install scanpy==1.9.1

!pip install scikit-learn==1.1.3

!pip install scipy==1.9.3

!pip install numpy==1.23.5

!pip install pandas==1.5.2

!pip install einops==0.6.0

!pip install local_attention==1.4.4

!pip install matplotlib==3.6

# Usage
1. Download the necessary data from the link: https://drive.google.com/drive/folders/1h7WwdCdH8lEJbPgLcfKHWBP9RTX2Buaa?usp=drive_link
   and create a folder called data under the pretrain folder like this: pretrain/data/...
2. Run the GetNCBIsummary to get summary data for each genes.
3. Run the GetEmbedding to get OPENAI embedding for description.
4. Run the Embedding_transform to get the new embedding
5. Run the runthepretrain to run the pretrain process
