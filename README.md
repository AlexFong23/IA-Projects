Polyphonic Music Generation with Transformers

Author
Alex Eduardo Cervantes Fong

Overview

This project presents a polyphonic music generation system based on a causal Transformer architecture trained on symbolic MIDI data from the MAESTRO Dataset

The model learns rhythmic and harmonic structures from piano performances and generates new melodies conditioned on tempo and dynamics

The objective of the project was to explore sequence modeling, structured tokenization, and controlled generative AI using deep learning

Methodology

Music is represented using symbolic MIDI instead of raw audio in order to reduce computational cost and improve interpretability

Long performances were segmented into fixed length fragments to create consistent training samples. Very short notes and low density fragments were filtered to improve musical coherence

An event based encoding scheme was designed using NOTE_ON NOTE_OFF and TIME_SHIFT tokens. Time was discretized at 25 millisecond resolution and velocity values were grouped into eight dynamic levels. The pitch range was restricted to the standard piano register

Special tokens were introduced to represent beginning and end of sequence as well as tempo and dynamics conditioning. The final vocabulary size was 1002 tokens

Model Architecture

The system is built using a six layer causal Transformer with an embedding dimension of 256 and eight attention heads

Learned positional embeddings are used to preserve temporal order. The model is trained using cross entropy loss and optimized with AdamW with a learning rate of 3e-4

Gradient clipping was applied to improve training stability. The model was trained for 210 epochs with checkpoint monitoring

The training objective is autoregressive. At each step the model predicts the next token given the previous musical context

Music Generation

Generation begins with conditioning tokens that specify tempo categories SLOW MED FAST and dynamics categories SOFT MED LOUD

Stochastic sampling strategies including temperature top k and top p were implemented to balance coherence and diversity

Generated token sequences are reconstructed into MIDI format and rendered into audio for qualitative evaluation

Results

The model achieved stable convergence and generated harmonically consistent and rhythmically structured polyphonic sequences

Conditioning tokens successfully influenced expressive characteristics, demonstrating controlled generative behavior
