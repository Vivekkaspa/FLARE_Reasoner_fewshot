
# FLARE: Few-shot Learning with Attention-guided Relational Subgraph Reasoner

The codes are associated with the following Manuscript submitted for PReMI'2025:

>**FLARE: Enhancing Few-Shot Missing Triple Prediction via Attention-Guided Subgraph Reasoning,**    
>Vivek Kaspa, Yashwanth Arikathota, Mukesh Eppili, Hima Bindu Kommanti


![FLARE1](https://github.com/user-attachments/assets/c2fe7b2b-91c9-40bf-a60c-289094046a6e)

## 1. Environments

To install requirements:
```pip install -r requirements.txt```

## 2. Datasets

The dataset, requirements, and data preparation follow the setting of [CSR](https://github.com/snap-stanford/csr). 
Download [NELL](http://snap.stanford.edu/csr/NELL.zip), [FB15K-237](http://snap.stanford.edu/csr/FB15K-237.zip), [ConceptNet](http://snap.stanford.edu/csr/ConceptNet.zip) data and the [embeddings](http://snap.stanford.edu/csr/embedding.zip) for all datasets. 

## 3. Training

To train our FLARE model on dataset(NELL, FB15K-237, ConceptNet):

Run

    python main.py --use_atten True --use_pretrain_node_emb True --dataset <dataset> --device 0 --step pretrain2 -prev_state_dir_model2 <dataset>/train_1/checkpoint.ckpt --train_num 1 -epo 20000 

## 4. Evaluation

To test the trained FLARE model:

Run

    python main.py --use_atten True --use_pretrain_node_emb True --dataset <dataset> --device 0 --step model2 -prev_state_dir_model2 <dataset>/train_1/checkpoint.ckpt

## 5. Acknowledgment

Our code is based on the code of [CSR](https://github.com/snap-stanford/csr) and [SAFER](https://github.com/HaochenLiu2000/SAFER). Thanks to the authors and developers!






