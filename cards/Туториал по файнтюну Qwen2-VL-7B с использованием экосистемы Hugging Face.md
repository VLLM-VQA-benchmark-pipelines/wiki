---
Author:
  - Овчинникова Юлия
tags:
  - tutorial
  - Qwen2-VL
date:
---

MachineLearning (Telegram)
[@ai_machinelearning_big_data](https://t.me/ai_machinelearning_big_data) 

[Статья](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#fine-tuning-a-vision-language-model-qwen2-vl-7b-with-the-hugging-face-ecosystem-trl) на HF из цикла [Open-Source AI Cookbook](https://huggingface.co/learn/cookbook/index) c подробным пошаговым описанием и примерами кода процесса тонкой настройки VLM Qwen2-VL-7B в области ответов на вопросы по изображениям с использованием библиотеки [Transformer Reinforcement Learning](https://huggingface.co/docs/trl/index) (TRL). В качестве целевого датасета используется ChartQA, который содержит диаграммы разных типов в паре с вопросами и ответами.

Для обучения модели демонстрируется методы Supervised Fine-Tuning (SFT) с использованием библиотеки TRL, QLoRA, которая квантует веса LoRA, обеспечивая более низкие требования к памяти и повышенную эффективность обучения.

Отдельным разделом выделен процесс подготовки данных к обучению с помощью функции collate_fn, которая выполняет корректное извлечение и пакетную обработку данных и  их форматирование для модели. Обучение модели осуществляется с помощью класса SFTTrainer.

В результате модель научилась отвечать на вопросы в соответствии с используемым датасетом. Оценить готовый файнтюн можно в демо на [HF Space](https://huggingface.co/spaces/sergiopaniego/Qwen2-VL-7B-trl-sft-ChartQA).

Дополнительно, в качестве альтернативы тонкой настройке, рассматривается использование промтинга с добавлением системного сообщения для контекстуализации ввода для модели, чтобы улучшить точность ее ответов. 

▶️ Блокнот на [Google Collab](https://colab.research.google.com/github/huggingface/cookbook/blob/main/notebooks/en/fine_tuning_vlm_trl.ipynb) для практических экспериментов. Для его запуска понадобится платный тариф с GPU А100.


▶️ Структура туториала по разделам:

🟢[Установка среды](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#1-install-dependencies)
🟢[Загрузка датасета](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#2-load-dataset-)
🟢[Загрузка модели и проверка производительности](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#3-load-model-and-check-performance-)
🟢[Файнтюн модели с помощью TRL](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#4-fine-tune-the-model-using-trl)

🟠[Загрузка квантованной модели для обучения](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#41-load-the-quantized-model-for-training-)
🟠[Настройка QLoRA и SFTConfig](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#42-set-up-qlora-and-sftconfig-)
🟠[Обучение модели](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#43-training-the-model-)

🟢[Тестирование готовой модели](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#5-testing-the-fine-tuned-model-)
🟢[Сравнение обученной модели с базовой + промптинг](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#6-compare-fine-tuned-model-vs-base-model--prompting-)
🟢[Дополнительные ресурсы для более глубокого изучения VLM](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#7-continuing-the-learning-journey-)

🔜 Статья на [HuggingFace](https://huggingface.co/learn/cookbook/fine_tuning_vlm_trl#fine-tuning-a-vision-language-model-qwen2-vl-7b-with-the-hugging-face-ecosystem-trl)


