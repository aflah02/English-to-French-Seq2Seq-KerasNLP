# English-to-French-Seq2Seq-KerasNLP

KerasNLP provides lots of building blocks for NLP (model layers, tokenizers, metrics, etc.) and
makes it convenient to construct NLP pipelines on the fly.

In this tutorial we'll use KerasNLP's `UnicodeTokenizer` to train a sequence-to-sequence Transformer model on English-to-French translation. This example draws inspiration from [Character-level recurrent sequence-to-sequence model example](https://keras.io/examples/nlp/lstm_seq2seq/) by [fchollet](https://twitter.com/fchollet) and uses the same dataset and __Abheest's Guide Here Once Published__ and uses the same model architecture and decoding code.

This tutorial broadly covers the following:
- Tokenization using `keras_nlp.tokenizers.UnicodeCharacterTokenizer` to obtain character level tokens.
- A sequence-to-sequence transformer model using KerasNLP's `keras_nlp.layers.TransformerEncoder`, `keras_nlp.layers.TransformerDecoder` and `keras_nlp.layers.TokenAndPositionEmbedding` layers
- Utilizes `keras_nlp.utils.greedy_search` ultility to translate text at runtime which implements the Greedy Search Decoding algorithm.

This tutorial will be pretty useful and will be a good starting point for learning about KerasNLP and how to incorporate it into your own NLP pipelines.

TLDR:

To see the demo just run [EngToFra.ipynb](https://github.com/aflah02/English-to-French-Seq2Seq-KerasNLP/blob/main/EngToFra.ipynb) also don't forget to set runtime to GPU for faster training

Model Architecture:
  - Transformer Encoder Decoder Model

Dataset:
  - [Anki French to English Dataset](http://www.manythings.org/anki/fra-eng.zip)

Tokenization Process Used:
  - Unicode Character Tokenization using [UnicodeCharacterTokenizer](https://keras.io/api/keras_nlp/tokenizers/unicode_character_tokenizer/)
