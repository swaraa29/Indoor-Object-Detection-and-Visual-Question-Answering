Indoor Visual Question Answering (VQA)

Overview
This project implements a unified Indoor Visual Question Answering (VQA) system that improves spatial grounding and reduces hallucinated responses by integrating object detection with vision-language reasoning.
The framework combines YOLOv8 for object detection and BLIP-2 for multimodal reasoning, coordinated through a Smart Question Routing (SQR) module.

Motivation
Traditional VQA pipelines often use object detectors and vision-language models independently. This can lead to:
Factually incorrect answers
Poor spatial localization
Hallucinated responses
This project addresses these limitations by designing a modular and grounded architecture.

Methodology
1. Object Detection (YOLOv8)
Detects and localizes objects in indoor scenes.
Supports factual queries such as counting, recognition, and classification.

2. Vision-Language Reasoning (BLIP-2)
Generates descriptive and open-ended answers.
Utilizes visual embeddings for contextual reasoning.

3. Smart Question Routing (SQR)
Classifies incoming queries into:
Factual queries → Routed to YOLOv8 with structured template-based answers.
Descriptive/open-ended queries → Processed by BLIP-2 using detected object context.
Reduces hallucination and improves grounding.

Dataset
Evaluated on the SUN RGB-D dataset for indoor scene understanding.
Results
Task completion rate: 83.3%
High-confidence responses: 80%
Improved grounding compared to isolated VLM-based approaches

Tech Stack
Python
PyTorch
YOLOv8
BLIP-2
OpenCV
Hugging Face Transformers

Applications
Assistive robotics
Smart environments
Indoor navigation systems
Multimodal conversational AI

Future Improvements
Fine-tuning on domain-specific datasets
Integration of scene graph reasoning
Real-time deployment optimization
Enhanced spatial reasoning mechanisms
