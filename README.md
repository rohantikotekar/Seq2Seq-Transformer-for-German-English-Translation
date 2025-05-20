
### Objective: The Transformer model aims to translate a given source sequence (English) into a target sequence (German).

### Training Data: It trains on (source sentence, target sentence) pairs extracted from a corpus. For example, a pair might be "A group of people are standing on a beach." (English) and "Eine Gruppe von Leuten steht an einem Strand." (German). The model learns to predict the likelihood of each target word given the source sentence and previously predicted target words.

### Architecture:
- Input & Output Embeddings: Converts tokens (words) into dense vector representations.
- Positional Encoding: Adds information about the order of words in the sequence.
- Encoder: Composed of multiple layers, each containing a Multi-Head Self-Attention mechanism and a Position-wise Feed-Forward Network. It processes the input sequence and generates an encoded representation (memory).
- Decoder: Also composed of multiple layers. Each layer includes a masked Multi-Head Self-Attention, a Multi-Head Cross-Attention (attending to the encoder's output), and a Position-wise Feed-Forward Network. It generates the output sequence one token at a time.
- Sublayer Connection (Add & Norm): Each sub-layer in both the Encoder and Decoder is wrapped in a residual connection followed by Layer Normalization.
Loss Function: Uses Negative Log-Likelihood Loss (nn.NLLLoss) to measure the difference between predicted and actual target sequences, ignoring padding tokens.

### Resume description
1. Developed a Transformer-based Neural Machine Translation (NMT) model from scratch, implementing core architectural components including Multi-Head Attention, Positional Encodings, Layer Normalization, and Feed-Forward Networks.
2. Engineered a complete Encoder-Decoder architecture, handling masked self-attention in the decoder to prevent attending to future tokens, enabling sequential generation of translations.
3. Implemented forward and backward propagation steps for the Transformer model, optimizing word and context embedding matrices over 200 epochs on a subset of the Multi30k dataset.
4. Achieved significant training progress with a final loss of approximately 0.15 (assuming this was your approximate final loss) by the end of training.
5. Demonstrated machine translation capabilities using a greedy decoding strategy, successfully translating unseen English sentences to German and qualitatively assessing the accuracy against reference translations.







