# ASR-Fine-Tuning-with-Nvidia-NeMo
With deep learning, the latest speech-to-text models are capable of recognition and translation of audio into text in real time! Good models can perform well in noisy environments, are robust to accents and have low word error rates (WERs).


<p align="center">
  <img src="images/download (1).png" width=300>
</p>

Build, train, fine-tune, and deploy a GPU-accelerated
automatic speech recognition service (ASR) with NVIDIA Riva and NVIDIA NeMo. 

<img src="images/flow_custom_asr.png" width=1000>

# NVIDIA Riva

[NVIDIA Riva](https://developer.nvidia.com/riva) is a GPU-accelerated SDK for building speech AI applications, customized for your use case, and delivering real-time performance. <br>
Riva offers a rich set of speech and natural language understanding services such as:

- Automated speech recognition ([ASR](https://docs.nvidia.com/deeplearning/riva/user-guide/docs/asr/asr-overview.html)).
- Text-to-Speech synthesis ([TTS](https://docs.nvidia.com/deeplearning/riva/user-guide/docs/tts/tts-overview.html)).
- Basic natural language processing ([NLP](https://docs.nvidia.com/deeplearning/riva/user-guide/docs/nlp/nlp-overview.html)) text and token classification functionality.
- Neural machine translation ([NMT](https://docs.nvidia.com/deeplearning/riva/user-guide/docs/translation/translation-overview.html)) between English and several other widely spoken languages, including Chinese, French, German, Russian, and Spanish.

# Nigerian English ASR Pipeline with NVIDIA Riva & NeMo

This project builds and deploys an Automatic Speech Recognition (ASR) system tailored for Nigerian English using NVIDIA's Riva and NeMo frameworks. The models and datasets used are large, but some have been preloaded for convenience. The original setup steps are documented below.

---

## 🎧 Finetuned Dataset

The dataset includes transcribed, high-quality audio recordings of Nigerian English sentences collected from volunteers in Lagos, Nigeria, and London, UK. The dataset consists of:

- `.wav` files (audio samples)
- `line_index.tsv` (metadata file containing anonymized `FileID` and corresponding transcriptions)

---

## 🔑 Step 1: Configure NGC CLI

Start by configuring the **NVIDIA NGC CLI** with your API key. This will allow you to download pretrained ASR components using the `ngc` command.

---

## 🚀 Step 2: Deploy Out-of-the-Box (OOTB) ASR Pipeline with NVIDIA Riva

Use the **Riva Quick Start scripts** to deploy an out-of-the-box ASR pipeline:

- Configure the **Riva server** for ASR.
- Start the server and run inference.
- The **NVIDIA Triton™ Inference Server** operates in the background, managing model loading and inference.

---

## 🧱 Step 3: Build & Deploy ASR Pipeline with Riva

In this step, you will:

- Build a custom ASR pipeline using pretrained components from **NVIDIA NeMo**.
- Deploy the pipeline using **Riva** to process speech-to-text tasks.

---

## 💬 Step 4: Improve Recognition with Word Boosting

Enhance the model's ability to recognize important or frequently used words:

- Use **word boosting** in a notebook to prioritize specific words.
- Improve recognition accuracy for domain- or dialect-specific vocabulary.

---

## 🛠️ Step 5: Fine-Tune ASR Model with NVIDIA NeMo

Fine-tune an existing **US English (en-US)** Riva ASR acoustic model to Nigerian English (en-NG):

- Use **NVIDIA NeMo** for the fine-tuning process.
- Train on your curated Nigerian English dataset.
- Validate performance with representative speech samples.

---

## 📦 Step 6: Deploy the Fine-Tuned Custom ASR Model

Finally, deploy the fine-tuned Nigerian English ASR model:

- Package and load the custom model using **Riva**.
- Run inference using your localized and optimized ASR system.

---

This pipeline equips you with all the tools to adapt powerful speech recognition technologies to localized dialects, starting with Nigerian English.
