
DeepSeek

### Пример использования Docker в Prefect

В Prefect вы можете использовать директиву task для определения задач, которые будут выполняться в Docker контейнерах. Вы можете передавать параметры в эти задачи через аргументы.

#### 1. Установка Prefect и Docker

Убедитесь, что у вас установлены Prefect и Docker:

```
pip install prefect
```
#### 2. Создание задачи с использованием Docker

Вы можете создать задачу, которая будет выполняться в Docker контейнере, и передать ей параметры:

```
from prefect import task, Flow
from prefect.tasks.docker import DockerRun

# Определение задачи, которая будет выполняться в Docker контейнере
@task
def my_docker_task(param1, param2):
    # Здесь вы можете использовать параметры param1 и param2
    print(f"Param1: {param1}, Param2: {param2}")

# Создание пайплайна
with Flow("MyDockerFlow") as flow:
    # Передача параметров в задачу
    result = my_docker_task("value1", "value2")

# Запуск пайплайна
flow.run()
```
#### 3. Использование DockerRun для запуска контейнера

Вы также можете использовать встроенную задачу DockerRun для запуска Docker контейнера и передачи параметров:

```
from prefect import task, Flow
from prefect.tasks.docker import DockerRun

# Создание задачи для запуска Docker контейнера
docker_run_task = DockerRun(image="my-docker-image:latest")

# Создание пайплайна
with Flow("MyDockerFlow") as flow:
    # Передача параметров в Docker контейнер
    result = docker_run_task(command=["--param1", "value1", "--param2", "value2"])

# Запуск пайплайна
flow.run()
```

### Передача параметров через командную строку

Вы также можете передавать параметры через командную строку при запуске пайплайна:

```
prefect run --param param1=value1 --param param2=value2
```
