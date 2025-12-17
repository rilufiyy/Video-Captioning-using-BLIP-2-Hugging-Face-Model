# 🎥 Video Captioning using BLIP-2 (Hugging Face)

This repository implements an **end-to-end video captioning pipeline** using the **BLIP-2 multimodal model from Hugging Face**.  
The system converts videos into descriptive text by **extracting representative frames** and generating captions using a powerful vision-language model.

---

## ✨ Features

- 🔹 Video segmentation and frame sampling
- 🔹 Image-to-text captioning using **BLIP-2 (Salesforce)**
- 🔹 Support for long videos via segment-based processing
- 🔹 Modular and easy-to-extend pipeline
- 🔹 Works on Google Colab and local environments
- 🔹 Hugging Face Transformers integration

---

## 🧠 Model Used

- **BLIP-2 (Bootstrapping Language-Image Pre-training)**
- Provider: **Salesforce Research**
- Hosted on: **Hugging Face**

Supported models:
- `Salesforce/blip2-flan-t5-xl`
- `Salesforce/blip2-opt-2.7b`

> ⚠️ BLIP-2 is an image-captioning model.  
> For video captioning, videos are decomposed into frames which are captioned and then aggregated.

---

## 🏗️ Pipeline Overview

```text
Video
 └── Segment video (time-based)
      └── Sample frames per segment
           └── BLIP-2 caption per frame / segment
                └── Merge captions into video-level description
