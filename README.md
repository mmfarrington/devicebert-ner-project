# devicebert-ner-project
Code to reproduce experiments from the paper "DeviceBERT: Applied Transfer Learning With Targeted Annotations and Vocabulary Enrichment to Identify Medical Device and Component Terminology in FDA Recall Summaries"

## Model Details

### Abstract
*FDA Medical Device recalls are critical and time-sensitive events, requiring
swift identification of impacted devices to inform the public of a recall event and
ensure patient safety. The OpenFDA device recall dataset contains valuable
information about ongoing device recall actions, but manually extracting relevant
device information from the recall action summaries is a time-consuming task.
Named Entity Recognition (NER) is a task in Natural Language Processing
(NLP) that involves identifying and categorizing named entities in unstructured text.
Existing NER models, including domain-specific models like BioBERT, struggle
to correctly identify medical device trade names, part numbers and component terms within these
summaries. To address this, we propose DeviceBERT, a medical device annotation, pre-processing and enrichment pipeline, which builds on BioBERT to identify and label medical device terminology in the device recall summaries with improved accuracy. Furthermore, we demonstrate that our approach can be applied effectively for performing entity recognition tasks where training data is limited or sparse.*

### Model Description

This model was created as part of a student final project for Stanford CS224N Spring 2024.
Project Title: "Optimizing BioBERT to Perform Named Entity Recognition of Medical Devices Using FDA Device Recall Summaries"

DeviceBERT utilizes BioBERT (dmis-lab/biobert-base-cased-v1.2) which has been trained on PubMed and PMC and subsequently finetuned to accurately identify industry specific medical device trade names, component parts and part numbers. 

The model was trained utilizing a processed and annotated NER dataset created using the OpenFDA Device Recalls Dataset (https://open.fda.gov/apis/device/recall/), and further
tokenized using the DistilBERT AutoTokenizer. It can be used to perform inferencing to accurately identfiy and label medical device, device component, part number and trade name related terms in a variety of downstream applications. 

- **Developed by:** Miriam Farrington for CS224N
- **Model type:** Deep Learning Language Model/LLM
- **Language(s) (NLP):** Python, TensorFlow
- **License:** MIT
- **Finetuned from model [optional]:** BioBERT (dmis-lab/biobert-base-cased-v1.2)

### Model Sources [optional]

- **Transformer Links:** [https://github.com/mmfarrington/devicebert-ner-project](https://huggingface.co/mfarrington/devicebert-base-cased-v1.0/edit/main/README.md)
- **Paper:** "DeviceBERT: Applied Transfer Learning With Targeted Annotations and Vocabulary Enrichment to Identify Medical Device and Component Terminology in FDA Recall Summaries"

## Uses

### Direct Use

This model can be directly used to perform NER inferencing on text to identify medical device related terms, trade names, components and part numbers in a variety of downstream tasks.
The model can be applied further to generate human feedback loops using inferencing to generate additional NER data for more complex downstream tasks or additional finetuning.

## Training Details

### Training Data

mfarrington/biobert-ner-fda-recalls-dataset






