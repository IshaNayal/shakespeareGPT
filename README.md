# Shakespeare GPT Tokenizer

A Byte Pair Encoding (BPE) tokenizer trained on Shakespeare's complete works, designed for building GPT models on classical literature.

## Overview

This project implements a custom BPE tokenizer trained on the complete works of Shakespeare. BPE is a subword tokenization algorithm that learns the most frequent byte-pair sequences in the training data, making it efficient for language modeling tasks.

## Features

- **Byte-Level Tokenization**: Uses ByteLevel encoding for robust handling of any character
- **BPE Training**: Implements Byte Pair Encoding to learn optimal token vocabulary
- **Post-Processing**: Includes proper post-processing for seamless text reconstruction
- **Shakespeare Dataset**: Pre-trained on complete Shakespeare corpus for literary NLP tasks

## Requirements

- Python 3.8+
- PyTorch (`torch`)
- Tokenizers (`tokenizers`)
- TorchInfo (`torchinfo`)
- tqdm (progress bars)
- Matplotlib (visualization)
- KaggleHub (for dataset downloads)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/IshaNayal/shakespeareGPT.git
cd GTP-Tokenizer
```

2. Install dependencies:
```bash
pip install torch tokenizers torchinfo tqdm matplotlib kagglehub
```

## Usage

Run the Jupyter notebook to:

1. **Build the Tokenizer**
   - Initialize a BPE tokenizer with ByteLevel encoding
   - Configure pre-tokenizers and post-processors
   - Train on Shakespeare dataset

2. **Tokenize Text**
   - Encode text into token sequences
   - Decode token sequences back to text

3. **Analyze Results**
   - Visualize tokenization patterns
   - Examine vocabulary statistics

## Dataset

The Shakespeare dataset is automatically downloaded from Kaggle using `kagglehub`:
- Source: [Shakespeare Full Text Dataset](https://www.kaggle.com/datasets/mohammedmohsen0404/shakespeare-txt)
- Contains complete works of Shakespeare
- ~5MB of raw text

## Project Structure

```
GTP-Tokenizer/
├── README.md
├── tokenizer.ipynb      # Main notebook with tokenizer training
└── tokenizer/           # Directory for saved tokenizer model
```

## Notebook Structure

The `tokenizer.ipynb` notebook includes:

1. **Setup**: Install required packages and import libraries
2. **Data Loading**: Download Shakespeare dataset via KaggleHub
3. **Tokenizer Configuration**: Set up BPE with ByteLevel encoding
4. **Training**: Train tokenizer on Shakespeare corpus
5. **Evaluation**: Test encoding/decoding functionality

## Model Details

### Tokenizer Configuration
- **Algorithm**: Byte Pair Encoding (BPE)
- **Pre-tokenizer**: ByteLevel (preserves whitespace)
- **Processor**: ByteLevel post-processor
- **Decoder**: ByteLevel decoder
- **Vocabulary Size**: Configurable (default: 500 tokens)

## Future Work

- Extend to train full GPT model on tokenized Shakespeare
- Fine-tune on other literary works
- Create inference pipeline for text generation
- Add model evaluation metrics

## License

This project uses the Shakespeare dataset which is publicly available.

## Author

Isha Nayal

## Acknowledgments

- Dataset source: Kaggle (Mohammed Mohsen)
- Tokenizer library: [Hugging Face Tokenizers](https://github.com/huggingface/tokenizers)
- Deep learning framework: [PyTorch](https://pytorch.org/)
