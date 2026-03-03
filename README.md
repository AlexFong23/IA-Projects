AI Engineering Portfolio

Alex Eduardo Cervantes Fong

This repository gathers selected projects developed in the field of Artificial Intelligence, with a focus on Generative Models, Natural Language Processing, and Deep Learning. Each project reflects hands on experimentation, architectural design decisions, and critical evaluation of results rather than isolated model implementation.

🎹 Project 1: Polyphonic Music Generation with Transformers

Category: Generative AI | Audio Modeling | PyTorch

This project presents a polyphonic music generation system based on a causal Transformer trained on symbolic MIDI data from the MAESTRO Dataset.

Music is modeled as a sequence of structured events rather than raw audio, allowing the system to learn rhythmic and harmonic relationships directly from piano performances. The preprocessing pipeline includes segmentation of long pieces into manageable fragments and the design of a custom tokenization scheme based on musical events.

The architecture is built around a multi layer Transformer trained in an autoregressive manner, predicting the next musical token given previous context. The system also incorporates conditioning tokens to guide expressive attributes such as tempo and dynamics during generation.

This project highlights experience in sequence modeling, symbolic representation design, and controlled generative systems applied to music.

🔍 Project 2: RAG Pipeline for Technical Documentation

Category: NLP | LLMs | Information Retrieval

This project consists of a Retrieval Augmented Generation pipeline designed to answer domain specific questions using a curated technical corpus.

The system combines document preprocessing, semantic chunking, and vector embeddings to enable similarity based retrieval. Retrieved content is then used as contextual grounding for a language model, improving the factual consistency of generated answers.

Different retrieval configurations and embedding strategies were explored to analyze their impact on response quality and hallucination reduction in Large Language Models.

The implementation was developed in Python using LangChain and vector databases for efficient semantic search.

This work demonstrates practical understanding of retrieval systems, prompt augmentation, and the integration of language models with external knowledge sources.

🖼️ Project 3: Anime Face Generation with GAN

Category: Computer Vision | Generative Models | TensorFlow

This project explores adversarial image generation using a Generative Adversarial Network trained on an anime face dataset from Kaggle.

The system is composed of two neural networks trained in opposition: a Generator that creates synthetic images from random noise and a Discriminator that learns to distinguish between real and generated samples. Through this competitive process, the Generator progressively improves its ability to produce visually coherent faces.

The architecture relies on convolutional layers for feature extraction and upsampling, along with normalization and regularization techniques to support stable training. Model performance was monitored both qualitatively and through distribution based evaluation metrics to assess realism and convergence.

This project emphasizes practical experience with adversarial training dynamics, generative modeling in computer vision, and the challenges associated with stability and evaluation in GAN based systems.

