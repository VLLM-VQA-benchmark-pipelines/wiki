---
Author:
  - Ширяев Антон
Implementer:
  - Ширяев Антон
tags:
  - VLMEvalKit
  - Docker_image
  - GitHub_repo
start date: 2024-11-21
end date: 2024-11-25
---
# Описание задачи

Мы хотим запустить Qwen2-Vl-2B

* [x] Клонировать VLMEvalKit ([ссылка](https://github.com/open-compass/VLMEvalKit))
* [x]  Собрать Docker контейнер и в него pipом установить [requirements.txt](https://github.com/open-compass/VLMEvalKit/blob/main/requirements.txt "requirements.txt")
Поправить [requirements.txt](https://github.com/open-compass/VLMEvalKit/blob/main/requirements.txt "requirements.txt") 
- **Please use** `transformers==4.33.0` **for**: `Qwen series`, `Monkey series`, `InternLM-XComposer Series`, `mPLUG-Owl2`, `OpenFlamingo v2`, `IDEFICS series`, `VisualGLM`, `MMAlaya`, `ShareCaptioner`, `MiniGPT-4 series`, `InstructBLIP series`, `PandaGPT`, `VXVERSE`.
* [x]  ЗаКоментировали интерфейс командной строки и смоделировали его arg.data (словарем, named tuple)
* [x] Шагаем дебаггером питона увидеть все шаги и используемые модули и классы которые от бенчмарка
* [x] Мы дошли до шага скачивания датасета в CVS.
* [x] Прерываемся и вручную уменьшаем его до 10 вопросов по картинкам.

Получилось, сделал `MTVQA_TEST` c выборкой из 10 картинок и вопросов.
* [ ] Зарегистрировать минидатасет в бенчмарке.
Не получилось. Сильная завязка на облачное хранение датасетов и проверку MD5 хешей.
Нужно реализовывать свой класс учитывающий всю их иерархию системы типов.

* [ ] **прогнали 1 раз на минидатасете убедиться что все отработало.**
Удалось запустить полный прогон модели `Qwen2-VL-2B` на полном датасете `MTVQA_TEST`.
Увы, на некоторых картинках мне не хватило GPU RAM 24 Gb и прогон остановился.

Интерес в том, чтобы увидеть какие компоненты бенчмарка VLMEvalKit соответствуют нашей схеме.
# Результаты

* Dockerfile который позволяет сделать прогон. (и репозиторий VLMEvalKit + все рабочее окружение для запуска Qwen2-Vl-2B на DocVQA) [ссылка](https://github.com/medphisiker/VLMEvalKit_docker/blob/main/docker/Dockerfile-cu124)
* гит репозиторий благодаря которому можно сделать прогон [ссылка](https://github.com/medphisiker/VLMEvalKit_docker).
* передать свои наработки всем остальным участникам команды для экономии времени и сил.
