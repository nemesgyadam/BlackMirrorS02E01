# Task

In this project I trained a Machine Learning model to mimic my behavior and conversation style.

More precisely I fine tuned a GPT3 model on my facebook chat history.

# Usage steps:

    *Download the chat history from facebook settings
    /download your information

    *Parse the data with the ‘parser.ipynb’ jupyter notebook

    *Fine tune the model with the the OpenAI CLI

    *Generate answer messages with the ‘chat.ipynb’ jupyter notebook

# Detalied instructions:

## Acquary Data

 https://www.facebook.com/dyi/?referrer=yfi_settings

![Alt text](images/fb_step1.jpg?raw=true "FB Download Step1")

![Alt text](images/fb_step2.jpg?raw=true "FB Download Step2")



## Fine tune
You can fine tune a GPT3 model with the following CLI command:

openai api fine_tunes.create -t 'conversations.jsonl' -m curie --n_epochs 3 --batch_size 128

More details at:
https://beta.openai.com/docs/api-reference/fine-tunes

### Estimated training prices

![Alt text](images/prices.png?raw=true "Training Prices")