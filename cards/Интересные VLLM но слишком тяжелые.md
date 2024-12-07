---
Author:
  - Овчинникова Юлия
  - Ширяев Антон
tags:
  - VLLM
  - модели
date: 2024-11-15
---
Здесь собираем интересные и перспективные VLLM, которые увы слишком громоздки.
Мы будем следить за научными командами, которые их разработали.
Возможно они опубликуют более компактные модели.

1. Pixtral-Large-Instruct-2411([ссылка](https://huggingface.co/mistralai/Pixtral-Large-Instruct-2411)) - 124B параметров, 52 файла saаetensors по 5 Гб каждый, итого где то ~ 260 Gb RAM для запуска.

Это примерно: 4 А100 по 80 Gb RAM.
Особая лицензия ([ссылка](https://mistral.ai/licenses/MRL-0.1.md))


2. LLaVA-CoT: VLM с пошаговыми рассуждениями - 10.7B параметров

Model Details:
- **License:** apache-2.0
- **Finetuned from model:** meta-llama/Llama-3.2-11B-Vision-Instruct

[Telegram](https://t.me/c/2429357431/63/732), [HuggingFace](https://huggingface.co/Xkev/Llama-3.2V-11B-cot)


3. PaliGemma 2: Новое семейство VLMs от Google

Семейство сочетает в себе кодировщик изображений SigLIP-So400m с спектром моделей Gemma 2, от 2B до 27B параметров. Модели PaliGemma 2 обучались в 3 этапа на трех разрешениях (224px², 448px² и 896px²).

[Telegram](https://t.me/c/2429357431/63/736)


