# Pneumonia & COVID-19 Detection CNN — Research Prototype

This repository explores CNN-based classification of chest X-ray images into Normal, Viral Pneumonia and COVID-19 categories.

![Python](https://img.shields.io/badge/Python-Deep%20Learning-3776AB?style=flat-square&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Research%20Prototype-c34b2e?style=flat-square)

## Project interface

[Open the research project page](https://aKmsdfhjb.github.io/Pneumonia-COVID-Detection-CNN/)

The browser page currently provides project documentation and a local-only image preview. It does not perform inference. A trained model artifact and a validated inference API are not present in the repository yet.

## Research pipeline

~~~mermaid
flowchart TD
 A[Document dataset source and license] --> B[Inspect class balance]
 B --> C[Patient-level train / validation / test split]
 C --> D[Preprocess and augment training images]
 D --> E[Train CNN]
 E --> F[Validate and tune]
 F --> G[Evaluate held-out test set]
 G --> H[Document metrics and limitations]
 H --> I[Package verified model weights]
 I --> J[Build and validate inference API]
 J --> K[Connect browser interface]
~~~

## Current repository contents

- notebooks/ — model-development material.
- models/ — currently a placeholder; no deployable trained weights are included.
- README.md — research overview and reproducibility notes.
- index.html — static project page and local image preview.

## Work required before inference can be added

1. Confirm dataset source, usage rights and exact class labels.
2. Record dataset size and class distribution.
3. Use patient-level separation to reduce data leakage.
4. Train and save the model with a documented preprocessing pipeline.
5. Evaluate on a held-out dataset and report per-class metrics.
6. Add an inference API and test it against known examples.
7. Only then connect the frontend to that API.

## Evaluation and safety

The earlier repository description included performance figures, but the current tracked files do not provide enough reproducible evidence to verify them. Those figures are intentionally not repeated here.

This project is educational research only. Chest X-ray classification is a high-stakes medical task. A model output must never be presented as a diagnosis or used to guide treatment. Clinical validation, representative data, external testing and qualified medical oversight would be required for any real-world use.

## License and data

Check the license and dataset terms for every dataset and model artifact before redistribution. Do not commit private patient data or identifiable medical images.
