# Persona-Creation-using-AI
This repository gives you the entire pipeline for creating a fine-tuned AI model for any online personality you want. Whether it's a celebrity or a YouTuber. The Repository is split into 5 code files. 

## getdata.ipynb
The first is getdata.ipynb. This contains the code to get the transcript data from a collection of YouTube videos and it contains mechanisms by which you can compress your likely massive dataset while maintaining a vast majority of the information to reduce future processing times and CPU/GPU strain. 

## speechtotext.ipynb
The second is speechtotext.ipynb. If there's any audio you want to use that doesn't have transcripts easily or readily available like YouTube does, this code can create transcripts for you out of any audio file or even just a link to the URL where the audio file is located. 

## gpt4webaccess.ipynb
The third is gpt4webaccess.ipynb. This code removes the need to use the GPT4 API to decrease the cost of running through this entire pipeline. It accesses the ChatGPT UI with Selenium and prints repeated messages while grabbing the results to generate a list of training data.

## addsource.ipynb
The fourth is addsource.ipynb. The code uses embeddings to grab similar data from the complete source text using cosine similarity and adds the two most similar source texts to each previously generated prompt and response pair. Having this data is important as when we actually run this model we want to generate the answer from a small section of the entire transcript list so as to vastly decrease runtime. 

## finetuning.ipynb
The fifth and final is finetuning.ipynb. This code is where the finetuning of the model actually happens. Here you can push to model to your Hugging Face page and make it publicly available for others to see. 

## Novelty
The innovations made in the project are the combination of the use of embeddings and fine-tuning in persona creation. Usually, either embeddings or fine-tuning is used. Embeddings are used for extracting response from a knowledge base and, in the persona creation space, fine-tuning is used to better take on the voice and style of a certain individual. My use of both allows for the quick extraction of responses from an extensive knowledge base, which can be especially important for public figures in the medical or finance space, combined with the embodiment of the voice of the person of desire. With this technology, we can have the best of both worlds.

## Future Steps
This project aimed to combine the use of embeddings and fine-tuning to create a superior product. However, it has not created a UI for people to interact with the model easily. This could be the next thing to explore. Also, using text-to-speech AI models to replicate your target persona's voice is quite useful. For example, if you fine-tuned your model to sound like Dr. Sanjay Gupta and to give answers that he would know, you could take that further by training a text-to-speech AI to sound like him and speak out the response in his voice. There's many directions that this could go and I'm excited to see it happen.
