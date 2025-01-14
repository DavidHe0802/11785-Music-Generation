# Enhancing Text-to-Audio Generation by Music Classification and Retrieval-Augmented Generation

## Project Overview
This project aims to refine AI-driven music generation by integrating **genre classification** and **retrieval-augmented generation (RAG)** pipelines. By combining advanced CNN architectures and the MUSICGEN model, we improve the fidelity, coherence, and personalization of generated music. 

Key highlights include:
- Training CNN models (ResNet-50, GoogleNet, and VGG16) for accurate music genre classification.
- Incorporating classified data into a RAG framework to retrieve relevant audio based on textual descriptions.
- Enhancing MUSICGEN's capability to generate music that reflects both text input and retrieved audio attributes.

## Features
1. **Music Genre Classification**:
   - ResNet-50, GoogleNet, and VGG16 architectures were employed for spectrogram-based genre classification.
   - Custom datasets, including the Jay Chou dataset, were developed and integrated with the GTZAN dataset.
   - Achieved a classification accuracy of 75% across ten standard genres, with notable success in recognizing unique styles like Jay Chou’s music.

2. **Retrieval-Augmented Generation**:
   - Utilized FAISS for efficient music document storage and retrieval.
   - Integrated user text queries with retrieved music via the MUSICGEN model, resulting in highly personalized and stylistically consistent outputs.

3. **Human Evaluation**:
   - Double-blind human studies demonstrated that the RAG-enhanced MUSICGEN model significantly outperformed the baseline in aligning generated music with specific stylistic elements.

## Datasets
- **GTZAN Music Genre Dataset**: Used for genre classification benchmarking.
- **Jay Chou’s Music Dataset**: Curated to highlight unique stylistic elements, processed into 30-second WAV segments.
- **MusicCaps Dataset**: Paired music recordings with captions for enhanced text-audio alignment.
- **Annotated Classical Music Dataset**: Proprietary dataset for classical music classification and retrieval.

## Implementation
### Music Classification
- Models were trained on spectrogram representations of audio signals.
- Fine-tuning involved cross-entropy loss, Adam optimizer, and early stopping to ensure robustness and efficiency.

### RAG Pipeline
- Metadata-driven retrieval using dense passage retrieval and FAISS.
- Combined retrieved audio and user text through MUSICGEN to generate novel music pieces that inherit attributes from both inputs.

### Music Generation
- MUSICGEN employed a transformer-based approach for generating music conditioned on input text and audio.

## Results
1. **Classification Performance**:
   - ResNet-50: F1-Score: 0.81, Recall: 0.77.
   - GoogleNet: F1-Score: 0.57, Recall: 0.50.
   - VGG16: F1-Score: 0.44, Recall: 0.18.

2. **Music Generation Evaluation**:
   - RAG-enhanced MUSICGEN achieved an average confidence score of 4.2 (out of 5) in a double-blind study, compared to 2.4 for the baseline model.

## Future Directions
1. Explore integration with advanced generative models (GANs, VAEs) for nuanced music generation.
2. Incorporate user feedback mechanisms to enhance interactivity and adaptability.
3. Expand datasets for broader genre and stylistic coverage.

## Repository
All code and datasets are available in the [MusicMindMeld GitHub repository](https://github.com/DavidHe0802/MusicMindMeld).

## Contributors
- **Runyu He** (David He): Project Lead and Developer
- **Junyi Zhu**, **Bochen Wang**, **Yixuan Yin**: Collaborators

## Citation
If you use this work, please cite: 'Runyu He, Junyi Zhu, Bochen Wang, Yixuan Yin. Enhancing Text-to-Audio Generation by Music Classification and Retrieval-Augmented Generation. Proceedings of the 6th International Conference on Computing and Data Science, 2024.'

## License
This project is licensed under the [Creative Commons Attribution License 4.0](https://creativecommons.org/licenses/by/4.0/).

