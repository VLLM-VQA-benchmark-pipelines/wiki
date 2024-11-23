---
Author:
  - Ширяев Антон
Implementer:
  - Ширяев Антон
tags: 
start date: 
end date: 2024-11-25
---
# Описание задачи

Мы хотим запустить Qwen2-Vl-2B

* Клонировать VLMEvalKit ([ссылка](https://github.com/open-compass/VLMEvalKit))
* Собрать Docker контейнер и в него pipом установить [requirements.txt](https://github.com/open-compass/VLMEvalKit/blob/main/requirements.txt "requirements.txt")
Поправить [requirements.txt](https://github.com/open-compass/VLMEvalKit/blob/main/requirements.txt "requirements.txt") 
- **Please use** `transformers==4.33.0` **for**: `Qwen series`, `Monkey series`, `InternLM-XComposer Series`, `mPLUG-Owl2`, `OpenFlamingo v2`, `IDEFICS series`, `VisualGLM`, `MMAlaya`, `ShareCaptioner`, `MiniGPT-4 series`, `InstructBLIP series`, `PandaGPT`, `VXVERSE`.
* ЗаКоментировали интерфейс командной строки и смоделировали его arg.data (словарем, named tuple)
* Шагаем дебаггером питона увидеть все шаги и используемые модули и классы которые от бенчмарка
* Мы дошли до шага скачивания датасета в CVS.
* Прерываемся и вручную уменьшаем его до 10 вопросов по картинкам.
* Зарегистрировать минидатасет в бенчмарке.
* **прогнали 1 раз на минидатасете убедиться что все отработало.**

Интерес в  том чтобы увидеть какие компоненты бенчмарка VLMEvalKit соответствуют нашей схеме.
# Результаты

* Dockerfile который позволяет сделать прогон. (и репозиторий VLMEvalKit + все рабочее окружение для запуска Qwen2-Vl-2B на DocVQA)
* ваш гит репозиторий благодаря которому можно сделать прогон.
* передать свои наработки всем остальным участникам команды для экономии времени и сил.
