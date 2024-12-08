---
Author:
  - Ширяев Антон
Implementer:
  - Капустин Евгений
tags:
  - Docker_image
  - VLLM
  - бенчмарк
  - MiniCPM_V_26
start date: 2024-12-07
end date:
---
# Описание задачи

* Создать Docker Image для запуска моделей семейства MiniCPM-V 2.6
* Запустить Docker Image и и модель внутри него задав ей вопрос по картинке, получить от нее ответ.
Тестовые картинки можно взять [ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/tree/main/src/example_docs) или использовать любые другие.
* Обернуть модель в класс с интерфейсом:

```
class NameModel_model:
	__init__(self, cache_directory, model_name="model_name"):
		pass

	predict_on_image(self, image_path, question):
		pass

	predict_on_images(self, images_paths, question):
		pass
```

* пример класса данного интерфейса для Qwen2-VL ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/blob/main/src/model_utils.py))
* пример предсказания модели для  Qwen2-VL ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/blob/main/src/run_predict.py))
# Результаты

Можно ориентироваться на результаты задачи ([ссылка](../3.%20В%20работе/Docker%20Image%20для%20моделей%20Qwen2-VL.md)).

