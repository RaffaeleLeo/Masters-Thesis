# This is the code that accompanies my thesis titled "Like Father Like SON"


Lamma3-finetuning.ipynb finetunes a lamma 3.0 model on the NVBench visualization dataset, I only fine-tune it on 200 instances to keep the model weak so the work done by the PPO learning and my SON model is more visual


SON.ipynb then takes this fine-tuned model and performs reinforcement learning on it, using the SON model I made outlined in my thesis. This file has the code for training SON and fine-tuning the lamma model using PPO learning.


For a detailed description of the SON and how it works, please read through Thesis.pdf


# WORK ADDED AFTER


After my thesis was done, I added chatgpt to be used to recommend rewards before training the Stable Observer Network (SON). Chatgpt was added in the initial 200 iterations of PPO learning, giving better feedback to training our SON model, increasing the performance on outputting the correct graph type and data type by 10 and 15 percent respectively.