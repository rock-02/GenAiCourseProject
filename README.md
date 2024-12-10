Abstract Summarizer


Working Explanation
Loading Data:

The first step is to load the dataset, which consists of news articles. The dataset typically includes columns like the article text and the headline (summary).
Unnecessary columns are removed to focus on the text and summary data.
Preprocessing:

Each summary is modified to include special start (<go>) and end (<stop>) tokens. These tokens help the model understand where a summary begins and ends, which is crucial for training the decoder.
Tokenization:

Tokenization is the process of converting text into numerical tokens. This is done for both the article text (document) and the summaries.
A tokenizer is trained on the texts to build a vocabulary of words and assign each word a unique integer. Words not in the vocabulary are assigned a special token (<unk> for "unknown").
The texts are then converted into sequences of integers based on the vocabulary.
Vocabulary Size:

The sizes of the vocabularies for the encoder (processing the article text) and the decoder (processing the summaries) are determined. These sizes are important for setting up the embedding layers in the model.
Model Architecture:

Encoder: This part of the model processes the input text (articles). It converts the sequence of tokens into context-aware embeddings, which capture the meanings of words in the context of the surrounding words.
Decoder: This part uses the context provided by the encoder to generate the summary one token at a time. It starts with the `<go
