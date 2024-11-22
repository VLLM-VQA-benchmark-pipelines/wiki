---
Author:
  - Изюмова Анастасия
tags:
  - VLLM
  - обучение_VLLM
  - создать_VLLM
date: 2024-11-20
---
Интеренcное видео ([ссылка](https://www.youtube.com/watch?v=T7sxvrJLJ14&ab_channel=AIEngineer)) про обучение компактной быстрой 2B VLM, которая оказалась лучшей в своем классе. [ссылка на источник](https://t.me/ai_newz/3443)

**Модель:**
* LLM: Phi1.6B 
* Vision encoder: SigLIP 400M

**Cинтетический датасет:**
* на задачу LNQA (Localized Narratives Question Answering) с вопросами-ответами по картинкам
* 300к пар.

**Итог:**
* Получилась сильная и шустрая модель.
* Правильные данные решают.

**P.S.:** Автор получил 5M долларов и сроит стартап `moondream.ai` по обучению компактных моделей.

**Материалы**:
- Github [ссылка](https://github.com/vikhyat/moondream)
- Demo [ссылка](https://huggingface.co/spaces/vikhyatk/moondream2)
- Blogpost про синтетический QA датасет [ссылка](https://vikhyat.net/posts/2024-08-17-lnqa.html)
- Видео [ссылка](https://www.youtube.com/watch?v=T7sxvrJLJ14)

> Кто за то, чтоб повторить? =)