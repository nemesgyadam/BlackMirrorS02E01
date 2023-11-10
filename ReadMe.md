# Task

![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)
![pip](https://img.shields.io/badge/pip-v21.0.1-blue)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT3.5-red)

In this project, I trained a Machine Learning model to mimic my behavior and conversation style by fine-tuning a GPT-3 model on my Facebook chat history.

## Usage Steps:

1. **Download Chat History from Facebook**: Go to Facebook settings and select 'Download Your Information'.

2. **Parse Data**: Utilize the `parser.ipynb` Jupyter notebook to process the downloaded chat history.

3. **Fine-Tune the Model**: Use the OpenAI Online Platform or the CLI to fine-tune the GPT-3.5 model.

4. **Generate Answer Messages**: Employ the `chat.ipynb` Jupyter notebook to create responses.

## Detailed Instructions:

### Acquire Data

To obtain your Facebook chat history, visit: [Facebook Data Download](https://www.facebook.com/dyi/?referrer=yfi_settings)

Steps to download:
![FB Download Step1](images/fb_step1.jpg?raw=true "FB Download Step1")
![FB Download Step2](images/fb_step2.jpg?raw=true "FB Download Step2")
![FB Download Step3](images/fb_step3.jpg?raw=true "FB Download Step3")
![FB Download Step4](images/fb_step4.jpg?raw=true "FB Download Step4")

- Wait for the data prepration (usually takes 10-20 minutes)
- Download the data
- Copy it to source_conversations folder

### Run Parser Notebook

See a comparison of the original Facebook conversation format and the GPT formatted data:
- ![Sample Data](images/sample_data.jpg?raw=true "Sample Data")

### Fine-Tune Your Model
You can fine tune the model with the following two ways:



### Online:
https://platform.openai.com/finetune


#### CLI 

Execute the following CLI command to fine-tune a GPT model:

```bash
openai api fine_tunes.create -t 'conversations.jsonl' -m curie --n_epochs 3 --batch_size 128
```

For more details, visit the OpenAI Fine-Tuning Documentation:

https://platform.openai.com/docs/guides/fine-tuning/preparing-your-dataset

Estimated Training Prices
For an estimation of the training costs, refer to the following image:

![Sample Data](images/prices.png?raw=true "Prices")


## License

MIT License

Copyright (c) [2022] [Nemes Gyula Ádám]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.