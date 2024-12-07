
@ai_machinelearning_big_data [Telegram](https://t.me/c/2429357431/63/735)

[Unsloth](https://unsloth.ai/blog/dynamic-4bit) представил практический метод динамического 4-битного квантования VLM, который решает проблему снижения точности популярных алгоритмов квантования AWQ, Bitsandbytes, GPTQ и HQQ.

В эксперименте использовался Bitsandbytes в качестве основы для всех линейных слоев, но квантование определенных параметров было динамически отключено. Этот подход позволил добиться значительного повышения точности при использовании всего на 10% больше VRAM по сравнению с стандартным 4-битным квантованием Bitsandbytes. 

В результате, этот метод позволяет сохранить точность модели, близкую к 16-битной точности, при значительном сокращении размера модели.

Тестирование на VL-моделях Llama 3.2 Vision, Qwen2 Vision и Pixtral, показали значительные преимущества по сравнению со стандартным 4-битным квантованием. Например, квантование Qwen2 Vision 2B до 4 бит приводило к полной поломке модели, в то время как метод динамического квантования позволял восстановить точность при увеличении использования памяти всего на 450 МБ. 

Аналогичным образом, получилось восстановить точность Llama 3.2 Vision 11B и Pixtral 12B, которые также деградировали на стандартном 4-битном квантовании.

▶️В открытый доступ на HF опубликованы модели, участвующие в исследовании:

🟢[Llama-3.2-11B-Vision-Instruct-unsloth-bnb-4bit](https://huggingface.co/unsloth/Llama-3.2-11B-Vision-Instruct-unsloth-bnb-4bit) (7.23 GB)
🟢[Llama-3.2-11B-Vision-unsloth-bnb-4bit](https://huggingface.co/unsloth/Llama-3.2-11B-Vision-unsloth-bnb-4bit)(7.23 GB)
🟠[Qwen2-VL-2B-Instruct-unsloth-bnb-4bit](https://huggingface.co/unsloth/Qwen2-VL-2B-Instruct-unsloth-bnb-4bit) (1.81 GB)
🟠[Qwen2-VL-7B-Instruct-unsloth-bnb-4bit](https://huggingface.co/unsloth/Qwen2-VL-7B-Instruct-unsloth-bnb-4bit) (6.3 GB)
🟠[QwQ-32B-Preview-unsloth-bnb-4bit](https://huggingface.co/unsloth/QwQ-32B-Preview-unsloth-bnb-4bit)
🟢[Pixtral-12B-2409-unsloth-bnb-4bit](https://huggingface.co/unsloth/Pixtral-12B-2409-unsloth-bnb-4bit) (8.42GB)

⚠️ К каждой модели в Model Card можно найти блокнот для запуска в Google Collab и созданные сообществом GGUF-версии.

📌Лицензирование моделей: 

🟠Семейство Llama: Llama 3.2 Community License Agreement
🟢Семейство Qwen: Apache 2.0 License.
🟢Pixtral: Apache 2.0 License.

🟡[Статья](https://unsloth.ai/blog/dynamic-4bit)
🟡[Набор моделей](https://huggingface.co/collections/unsloth/unsloth-4-bit-dynamic-quants-67503bb873f89e15276c44e7)
🟡[Сообщество в Discord](https://discord.gg/unsloth)


