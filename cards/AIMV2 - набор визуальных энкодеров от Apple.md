
@ai_machinelearning_big_data [Telegram](https://t.me/c/2429357431/63/728)

[AIMV2](https://huggingface.co/collections/apple/aimv2-6720fe1558d94c7805f7688c) – семейство моделей визуальных энкодеров, предварительно обученных с помощью мультимодальной авторегрессионной цели, которая восстанавливает фрагменты изображений и текстовые токены, что, в итоге, позволяет AIMV2 справляться с задачами распознавания изображений, локализации объектов и мультимодального понимания.

Архитектура AIMV2 основана на ViT и использует каузальный мультимодальный декодер, который сначала регрессирует фрагменты изображения, а затем декодирует текстовые токены авторегрессионно. Визуальный энкодер использует префиксное внимание, что позволяет использовать двунаправленное внимание во время вывода без дополнительной настройки.

Семейство AIMV2 обучалось на комбинации общедоступных (DFN-2B, COYO) и собственных (HQITP) датасетов, содержащих пары "изображение-текст" и синтетические аннотации, сгенерированные предварительно обученным инструментом.

Эксперименты после обучения показали, что AIMV2-3B достигает точности 89,5% на ImageNet с замороженным транком, что лучше, чем у генеративных методов MAE и AIM.  AIMV2 превосходит CLIP и SigLIP в большинстве тестов на мультимодальное понимание.

Модель  совместима с LiT для  zero-shot распознавания и может быть настроена для обработки изображений с различными разрешениями и соотношениями сторон.

В отрытый доступ на HF опубликованы модели: 

🟠AIMv2 в разрешении 224px: 4 модели с количеством параметров - 0.3B, 0.6B, 1.2B и 2.7B
🟠AIMv2 в разрешении 336px: 4 модели с количеством параметров - 0.3B, 0.6B, 1.2B и 2.7B
🟠AIMv2 в разрешении 448px: 4 модели с количеством параметров - 0.3B, 0.6B, 1.2B и 2.7B
🟢AIMv2 в Native разрешении : aimv2-large-patch14-native c 0.3B (разрешение в диапазоне от 112 до 4096)
🟢AIMv2 distilled ViT-Large (модели, которые были получены путем дистилляции из AIMV2-3B в архитектуру ViT-Large) : AIMv2-L и AIMv2-L-distilled.
🟠Zero-shot Adapted AIMv2 (модель после LiT- тюнинга): AIMv2-L с 0.3B параметров.


⚠️ ! Примеры инференса с [JAX](https://github.com/apple/ml-aim?tab=readme-ov-file#using-jax) и [MLX](https://github.com/apple/ml-aim?tab=readme-ov-file#using-mlx) доступны в [репозитории](https://github.com/apple/ml-aim) AIMv2

▶️Установка и локальный инференс c Pytorch:

# Clone the repository

```
pip install 'git+https://github.com/apple/ml-aim.git#subdirectory=aim-v2'
```

# Example Using PyTorch

```
from PIL import Image

from aim.v2.utils import load_pretrained
from aim.v1.torch.data import val_transforms

img = Image.open(...)
model = load_pretrained("aimv2-large-patch14-336", backend="torch")
transform = val_transforms(img_size=336)

inp = transform(img).unsqueeze(0)
features = model(inp)
```

📌Лицензирование: [Apple Sample Code License](https://developer.apple.com/support/downloads/terms/apple-sample-code/Apple-Sample-Code-License.pdf)


🟡[Коллекция на HF](https://huggingface.co/collections/apple/aimv2-6720fe1558d94c7805f7688c)
🟡[Arxiv](https://arxiv.org/pdf/2411.14402)
🖥[GitHub](https://github.com/apple/ml-aim)


