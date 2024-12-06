---
Author:
  - Овчинникова Юлия
tags:
  - smolvlm
date: 0224-12-06
---

Пост в Telegram ([link](https://t.me/c/2429357431/63/701)) 
@ai_machinelearning_big_data

[SmolVLM](https://huggingface.co/collections/HuggingFaceTB/smolvlm-6740bd584b2dcbf51ecb1f39) - серия компактных VLM с 2 млрд. параметров, отличающихся высокой эффективностью использования памяти и могут быть развернуты на локальных устройствах с ограниченными ресурсами.

Архитектура SmolVLM основана на Idefics3, с несколькими отличиями:
🟢В качестве языковой основы используется SmolLM2 1.7B вместо Llama 3.1 8B;
🟢Визуальная информация сжимается в 9 раз с помощью стратегии pixel shuffle, по сравнению с 4-кратным сжатием в Idefics3;
🟢Используются патчи  размером 384x384 пикселей, а не 364x364;
🟢Визуальная основа модели изменена на shape-optimized SigLIP с патчами 384x384 пикселей и внутренними патчами 14x14;
🟢Контекстное окно SmolLM2 было расширено до 16 тыс. токенов для поддержки работы с несколькими изображениями.

Модель кодирует каждый патч изображения 384x384 в 81 токен, что позволяет ей обрабатывать тестовые запросы и изображения с использованием всего 1.2 тыс. токенов, в то время как Qwen2-VL использует 16 тыс. токенов. Это преимущество приводит к значительно более высокой скорости предварительной обработки (в 3,3-4,5 раза) и генерации (в 7,5-16 раз) по сравнению с Qwen2-VL.

Для самостоятельной тонкой настройки SmolVLM можно использовать [transformers и TRL](https://huggingface.co/blog/smolvlm#fine-tuning). Разработчиками представлен [блокнот](https://github.com/huggingface/smollm/blob/main/finetuning/Smol_VLM_FT.ipynb) для файнтюна на VQAv2 с использованием LoRA, QLoRA или полной тонкой настройки. SmolVLM интегрирован с TRL для DPO через CLI.

⚠️ При batch sizes=4 и 8-битной загрузке QLoRA файнтюн потребляет около ~16 GB VRAM

📌Лицензирование:  Apache 2.0

🟡[Статья на HF](https://huggingface.co/blog/smolvlm)
🟡[Набор моделей](https://huggingface.co/collections/HuggingFaceTB/smolvlm-6740bd584b2dcbf51ecb1f39)
🟡[Demo](https://huggingface.co/spaces/HuggingFaceTB/SmolVLM)


![](files/SmolVLM-20241206.jpg)



