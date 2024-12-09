---
Author:
  - Ширяев Антон
Implementer:
  - Лукин Семен
tags:
  - описать_результаты
start date: 
end date: 2024-11-25
---
# Описание задачи

Хотим убедиться что он может запустить процесс внутри докер контейнера, передать параметры запуска докер-контейнеру.
Чтобы оркестратор дождался когда процесс внутри докера завершить, а не шел дальше на следующий шаг.
[Prefect Настройка параметров для Docker-контейнера](../../../cards/Prefect%20Настройка%20параметров%20для%20Docker-контейнера.md)

Запустить DAG из двух шагов:
1. Контейнер с питоном
	* Примонтировать папку /Data
	* Внутри скрипт writer.py, который создает и записывает в файл в /Data/task1.txt
		* содержание файла ...
		```
		step 1
		step 2
		..
		step 10
		```
2. Контейнер с питоном
	* Примонтировать папку /Data
	* Внутри скрипт reader.py, который читает из /Data/task1.txt 
	* пишет в /Data/task2.txt 
		* содержание файла ...
		```
		readed step 1
		readed step 2
		..
		readed step 10
		```

Лежит два файла и всё верно

https://github.com/VLLM-VQA-benchmark-pipelines/VLMEvalKit_experiments/tree/main/docker
* проброс гпу
* торч if cuda.is_aviable в оба файла
```
print('torch.__version__', torch.__version__)
print('torch.cuda.is_available()', torch.cuda.is_available())
print('torch.cuda.current_device()', torch.cuda.current_device())
print('torch.cuda.device_count()', torch.cuda.current_device())
print('torch.cuda.get_device_name(0)', torch.cuda.get_device_name(0))
```
# Результаты
* В ходе тестов не удалось запустить последовательно несколько контейнеров в одной таске.
* Вердикт подходит ли Prefect нам?  нет