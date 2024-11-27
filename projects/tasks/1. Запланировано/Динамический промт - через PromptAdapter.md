---
Author:
  - Ширяев Антон
  - Изюмова Анастасия
Implementer: 
tags:
  - промпт_инеженеринг
  - pipeline
start date: 2024-11-27
end date: 2024-11-27
---
# Описание задачи

Динамический промт - через PromptAdapter.
Согласовали, что архитектурно лучше делать так, чем множество одинаковых датасетов, но с разными промптами для

```
# Читает CSV файл для модели
# Можно реализовать как CVS-файл оптимальных промптов для каждой модели.
# Данный класс считывает таблицу с полем "doc_type_question_type" и "optimal_propt"
# Для каждой отдельной модели =)

class PrmptQwen2vlAdapter:
	dct = {"passport_Фамилия":"Оптимально подобранный промпт для Qwen2VL",
}

class PrmptMiniCPMAdapter:
	dct = {"passport_Фамилия":"Оптимально подобранный промпт для MiniCPM",
}



# не замедлит
optimal_promt = PrmptQwen2vlAdapter.gen_prompt(image, doc_class_question_type)

answear = model.predict(image, optimal_promt)

for model in models:
	for datset in datasets:
		run_bench(model, dataset)



```

# Результаты
