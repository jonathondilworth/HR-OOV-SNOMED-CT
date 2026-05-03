# Retraining Models

## Configurations for Hierarchy Transformer models

**HiT-all-MiniLM-L12-v2-INTERNATIONAL-20250901-FULL-4-EPOCHS**

```yaml
# DATASET DETAILS
dataset_path: "./data/hit_dataset_INTERNATIONAL_20250901_FULL"
dataset_name: "mixed"

# NEGATIVE TYPE (HARD, RANDOM)
negative_type: "random"

# BASE MODEL (TRAINING)
model_path: "sentence-transformers/all-MiniLM-L12-v2"

# TRAINING CONFIG
num_train_epochs: 4 # 2 # 4
train_batch_size: 256
eval_batch_size: 512
learning_rate: 1e-5
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
```

**HiT-all-MiniLM-L12-v2-INTERNATIONAL-20250901-MINI-4-EPOCHS**

```yaml
# DATASET DETAILS
dataset_path: "./data/hit_dataset_INTERNATIONAL_20250901_MINI"
dataset_name: "mixed"

# NEGATIVE TYPE (HARD, RANDOM)
negative_type: "random"

# BASE MODEL (TRAINING)
model_path: "sentence-transformers/all-MiniLM-L12-v2"

# TRAINING CONFIG
num_train_epochs: 4 # 2 # 4
train_batch_size: 256
eval_batch_size: 512
learning_rate: 1e-5
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5

```

**HiT-all-MiniLM-L12-v2-US-20140901-FULL-4-EPOCHS**

```yaml
# DATASET DETAILS
dataset_path: "./data/hit_dataset_US_20140901_FULL"

dataset_name: "mixed"

# NEGATIVE TYPE (HARD, RANDOM)
negative_type: "random"

# BASE MODEL (TRAINING)
model_path: "sentence-transformers/all-MiniLM-L12-v2"

# TRAINING CONFIG
num_train_epochs: 4
train_batch_size: 256
eval_batch_size: 512
learning_rate: 1e-5
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
```

**HiT-all-MiniLM-L12-v2-US-20140901-MINI-CPP-4-EPOCHS**

```yaml
# DATASET DETAILS
dataset_path: "./data/hit_dataset_US_20140901_MINI_CPP"
dataset_name: "mixed"

# NEGATIVE TYPE
negative_type: "random"

# BASE MODEL (TRAINING)
model_path: "sentence-transformers/all-MiniLM-L12-v2"

# TRAINING CONFIG
num_train_epochs: 4
train_batch_size: 256
eval_batch_size: 512
learning_rate: 1e-5
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
```

## Configurations for Ontology Transformer models

**OnTr-all-MiniLM-L12-v2-OnT-SNO-25-MINI-4-EPOCHS**

```yaml
##
# SNOMED 2025 SEPTEMBER RELEASE
# (Miniature Model)
##

# if you plan on re-training all four models
# it is reccomended you rename the dataset_path to something such as:
#   data/ont_dataset_INTERNATIONAL_20250901_MINI/OnT
# such that it is easy to distinguish between the full and mini versions

# note that the data preprocessing scripts will write to 
#   data/ont_dataset/OnT
# As such, we provide it as the default path:

dataset_path: "data/ont_dataset/OnT"
dataset_name: "OnT-SNO-25-mini"

##
# BASE MODEL
##

model_path: "sentence-transformers/all-MiniLM-L12-v2"

##
# Training Config
##

num_train_epochs: 4
train_batch_size: 32
eval_batch_size: 16
learning_rate: 1e-5
role_emd_mode: "sentenceEmbedding" 
role_model_mode: "rotation" 
existence_loss_kind: "hit" 
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
logical_loss:
  conj_weight: 1.0  
  exist_weight: 1.0
```

**OnTr-all-MiniLM-L12-v2-OnT-SNO-25-FULL-4-EPOCHS**

```yaml
##
# SNOMED 2025 SEPTEMBER RELEASE
# (FULL VERSION)
##

dataset_path: "data/ont_dataset/OnT"
dataset_name: "OnT-SNO-25"

##
# BASE MODEL
##

model_path: "sentence-transformers/all-MiniLM-L12-v2"

##
# Training Config
##

num_train_epochs: 4
train_batch_size: 32
eval_batch_size: 16
learning_rate: 1e-5
role_emd_mode: "sentenceEmbedding" 
role_model_mode: "rotation" 
existence_loss_kind: "hit" 
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
logical_loss:
  conj_weight: 1.0  
  exist_weight: 1.0
```

**OnTr-all-MiniLM-L12-v2-OnT-SNO-14-MINI-4-EPOCHS**

```yaml
dataset_path: "data/ont_dataset_US_20140901_MINI_CPP/OnT"
dataset_name: "OnT-SNO-14-mini"

model_path: "sentence-transformers/all-MiniLM-L12-v2"

num_train_epochs: 4
train_batch_size: 32
eval_batch_size: 16
learning_rate: 1e-5
role_emd_mode: "sentenceEmbedding" 
role_model_mode: "rotation" 
existence_loss_kind: "hit" 
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
logical_loss:
  conj_weight: 1.0  
  exist_weight: 1.0
```

**OnTr-all-MiniLM-L12-v2-OnT-SNO-14-FULL-4-EPOCHS**

```yaml
dataset_path: "/mnt/data/HOPE/data/ont_dataset_US_20140901_FULL/OnT"
dataset_name: "OnT-SNO-14"

model_path: "sentence-transformers/all-MiniLM-L12-v2"

num_train_epochs: 4
train_batch_size: 32
eval_batch_size: 16
learning_rate: 1e-5
role_emd_mode: "sentenceEmbedding" 
role_model_mode: "rotation" 
existence_loss_kind: "hit" 
hit_loss: 
  clustering_loss_weight: 1.0
  clustering_loss_margin: 3.0
  centripetal_loss_weight: 1.0
  centripetal_loss_margin: 0.5
logical_loss:
  conj_weight: 1.0  
  exist_weight: 1.0
```

