# Question_Answering_T5_BioASQ


* BioAsq dataset for largescale Biomedical QA was used to finetune the pretrained t-5 base model available on the hugging face transformers module
* The training dataset consited of around 450 unique questions and 2600 contexts respectively
* The model was trained with the hyperparameters and optimizer suggested by the authors of the paper "Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer"
* The context sequence length was truncated to 396 tokens per sample and the answer expected was clipped to max_length of 32 tokens
* PyTorch lightning was used to create the datamodule and an instance of the model for training and evaluation
* The state (Epoch) with the least validation loss was saved as checkpoint for further use
* Tensorboard was used to visualize the training and validation performance on the respective dataset
