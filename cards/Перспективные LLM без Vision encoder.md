---
Author:
  - Ширяев Антон
  - Овчинникова Юлия
  - Изюмова Анастасия
  - Кудрявцев Александр
tags:
  - LLM
  - основа_для_VLLM
date: 2024-11-10
---
Здесь мы собираем полезные LLM
* Не умеют отвечать на вопросы по картинкам.
* Нужно добавлять `Vision encoder` и доучивать до `VLLM`.

Они полезны как потенциальная база для разработки своей `VLLM`.

Список LLM:
1. RuQwen2.5-3B-Instruct-AWQ ([ссылка](https://huggingface.co/FractalGPT/RuQwen2.5-3B-Instruct-AWQ))
2. RuadaptQwen-2.5-32B-Instruct ([ссылка](https://t.me/ruadaptnaya/7))
3. Qwen2.5-Coder-32B-Instruct ([ссылка](https://huggingface.co/Qwen/Qwen2.5-Coder-32B-Instruct))
4. T-Lite и T-Pro от Т-банка ([ссылка](https://huggingface.co/t-tech))
* T-Lite([ссылка](https://huggingface.co/t-tech/T-lite-it-1.0)) 7 млрд параметров
* T-Pro ([ссылка](https://huggingface.co/t-tech/T-pro-it-1.0)) 32 млрд параметров 
построенные на базе моделей Qwen 2.5 и дообученные на русский язык.