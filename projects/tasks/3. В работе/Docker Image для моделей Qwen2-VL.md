---
Author:
  - Ширяев Антон
Implementer:
  - Ширяев Антон
tags:
  - Docker_image
  - Qwen2-VL
  - VLLM
  - бенчмарк
start date: 2024-12-02
end date:
---
# Описание задачи

* Создать Docker Image для запуска моделей семейства Qwen2-VL ([ссылка](https://huggingface.co/collections/Qwen/qwen2-vl-66cee7455501d7126940800d)).
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

* Создан репозиторий для модели ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl))
* Разработан Docker Image ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/blob/main/docker/Dockerfile-cu124))
* Реализован класс интерфейса для Qwen2-VL ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/blob/main/src/model_utils.py))
* Реализован скрипт предсказания модели для  Qwen2-VL ([ссылка](https://github.com/VLLM-VQA-benchmark-pipelines/model_qwen2-vl/blob/main/src/run_predict.py))
* Протестирован запуск моделей (нужно тестировать все варианты):

2B-варианты:
* Qwen2-VL-2B-Instruct
* Qwen2-VL-2B-Instruct-GPTQ-Int4

7B-варианты:
* Qwen2-VL-2B-Instruct
