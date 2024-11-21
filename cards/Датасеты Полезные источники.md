---
Author:
  - Овчинникова Юлия
  - Ширяев Антон
tags:
  - dataset
date:
---
## Обзор датасетов ко встрече

- Ширяев Антон беру ==MIDV-2020== (Можно использовать, есть фото 1 страницы российских паспортов. Уточнить у Марка нужны ли “1-вая страница разворота паспорта” и “страница с регистрацией гражданина”) и ==DocVQA==
  
Для паспортов Граждан РФ нужно собирать данные со страниц:
1. страница с информацией о том кем выдан паспорт, кодом подразделения и т.д.    
2. страница с Фото, фамилией и другими данными гражданина    
3. страница с регистрацией гражданина

Так же интересуют паспорта граждан ближнего зарубежья из этих паспортов нужно взять туже информацию, что и из паспортов РФ.

- Лукин Семён ==MTVQA== (Хороший датасет для теста возможности чтения русского языка с картинки)
- Овчинникова Юлия ==RusTitW==, ==TextVQAval==, ==InstructDoc==    
- Капустин Евгений: ==OCR-Cyrillic-Printed-10== и ==Cyrillic Handwriting Dataset== 

## Ссылки на датасеты

1. **MIDV-2020: A Comprehensive Benchmark Dataset for Identity Document Analysis**   
([ссылка описание](http://l3i-share.univ-lr.fr/MIDV2020/midv2020.html), [статья на Хабре](https://habr.com/ru/companies/smartengines/articles/714250/), [ссылки ftp для скачки](https://smartengines.ru/science/dataset/) )   

2. **Dataset ID cards**
[https://smartengines.ru/science/dataset/](https://smartengines.ru/science/dataset/)

| MIDV-500 | MIDV-2019 | MIDV-2020 | MIDV-LAIT | DLC-2021 | MIDV-Holo |
| -------- | --------- | --------- | --------- | -------- | --------- |

3. **MTVQA**
[https://github.com/bytedance/MTVQA/tree/main](https://github.com/bytedance/MTVQA/tree/main) 

4. **Synthetic datasets for text recognition tasks, contains 1.000.000 images**
[OCR-Cyrillic-Printed-6](https://huggingface.co/datasets/DonkeySmall/OCR-Cyrillic-Printed-6)
[OCR-Cyrillic-Printed-8](https://huggingface.co/datasets/DonkeySmall/OCR-Cyrillic-Printed-8)
[OCR-Cyrillic-Printed-10](https://huggingface.co/datasets/DonkeySmall/OCR-Cyrillic-Printed-10)
 
5. **73830 segments of handwriting texts (crops) in Russian**
[Cyrillic Handwriting Dataset](https://www.kaggle.com/datasets/constantinwerner/cyrillic-handwriting-dataset)

6. **synthetic_cyrillic_large** 
[ссылка](https://huggingface.co/datasets/nastyboget/synthetic_cyrillic_large) 

7. **Datasets of task - Visual Question Answering**
[https://paperswithcode.com/datasets?task=visual-question-answering-1&page=1](https://paperswithcode.com/datasets?task=visual-question-answering-1&page=1)

8. **RusTitW: Russian Language Visual Text Recognition** 
[ссылка](https://www.kaggle.com/datasets/hardtype/rustitw-russian-language-visual-text-recognition)  (Мега здоровый датасет на VQA по русскому тексту. Возможно пригодится для тюнинга LLM.)

  

## Обзор датасетов
### [DocVQA dataset](https://rrc.cvc.uab.es/?ch=17&com=downloads) 

==Для скачивания материалов нужна регистрация на сайте!==
#### Скачать
**Task 4 - Multipage Document Visual Question Answering (MP-DocVQA)**
The dataset for Multipage DocVQA is available to download from the following URLs:
V1.0 uploaded on 19 February 2023. The dataset consists of 46436 questions posed over 5929 documents with 47952 pages in total. Besides the questions and answers, we also provide the document page images and the OCR extracted with Amazon Textract OCR of all the pages (64057) that belong to the documents within MP-DocVQA dataset, skipping the limitation of 20 pages. Hence, you can use longer versions of the documents with the same image and OCR quality if required.
- [Questions and Answers](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazQvcWFzLnppcA==)
- [Images](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazQvaW1hZ2VzLnRhci5neg==) (21 Гб)    
- [OCR results](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazQvb2NyLnRhci5neg==) (Amazon Textract)    
- [IMDBs](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazQvbXBkb2N2cWFfaW1kYnMuemlw) (processed dataset for [MP-DocVQA framework](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9naXRodWIuY29tL3J1YmVucHQ5MS9NUC1Eb2NWUUEtRnJhbWV3b3Jr))    

**Task 1 - Single Page Document Visual Question Answering**
Dataset for Single Page Document VQA (SP-DocVQA) task is available to download at the below URLs.
[20 April 2020] train V1.0. Dataset released comprising 50,000 questions framed on 12,767 document images.
[31 August 2023] updated to include the training and validation question types.
- [Annotations](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazEvc3Bkb2N2cWFfcWFzLnppcA==) (questions, answers, question types...)    
- [Images](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazEvc3Bkb2N2cWFfaW1hZ2VzLnRhci5neg==) (8 Гб)    
- [OCR](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazEvc3Bkb2N2cWFfb2NyLnRhci5neg==) (Microsoft OCR)    
- [IMDBs](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazEvc3Bkb2N2cWFfaW1kYi56aXA=) (processed dataset for [MP-DocVQA framework](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9naXRodWIuY29tL3J1YmVucHQ5MS9NUC1Eb2NWUUEtRnJhbWV3b3Jr))    

**Task 2 - Document Collection Visual Question Answering (DocCVQA)**
Document Collection Visual Question Answering (DocCVQA) is defined over a collection of documents, over which natural language questions (queries) are defined.
We provide a series of sample queries along with the relevant documents for each one.
V0.1 uploaded on March 30, 2020. Comprises 14,362 document images, 8 sample queries and the list of relevant responses (document IDs) for each sample query.
V0.2 uploaded on April 23, 2020. The candidate's names in the sample queries' answers have changed the format from 'Surname Name' to 'Name Surname' to be consistent with the names written in the document images. The test queries have been made public.
- [Image collection](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazJfaW1hZ2VzLnppcA==)    
- [Sample queries and responses](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvc2FtcGxlX3B1YmxpY192MDIuanNvbg==)    
- [Test queries](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvdGVzdF9wdWJsaWMuanNvbg==)    
We also provide evaluation scripts so that participants can evaluate their methods in the exact same way as on the server.
- DocCVQA [Evaluation scripts](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazIlMjBldmFsdWF0aW9uJTIwc2NyaXB0LnppcA==)    

**Task 3 - Infographics VQA**
Participants to download the images using the URLs provided in the JSON file. OCR outputs for each image are provided using using [Amazon Textract](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9hd3MuYW1hem9uLmNvbS90ZXh0cmFjdC8=) OCR system. OCR outputs are auxiliary data; participants are free to use any OCR.
DISCLAIMER: All images provided here have been collected from freely accessible internet sites and social media. As such, they are copyrighted by their respective authors, and originally held at the URLs provided in the annotations files below. The images are hosted in this site, physically located in Spain, EU, under article 34 of the Spanish law of Intellectual Property. Specifically, the images are provided with the sole purpose to be used for research in developing new models for Document Visual Question Answering as defined in the present challenge. 
TERMS AND CONDITIONS: You are not allowed to redistribute any images you download from this site. By downloading any of the files below you explicitly state that your final purpose is to perform research in the conditions mentioned above and you agree to adhering to these terms and conditions.
[10 Nov 2020] train V0.1 was uploaded. Training a subset with around 10K questions defined on nearly 2,000 images. 
[23 Dec 2020] train 1.0 - 23946 questions; 4406 images.
[05 Jan 2021] val 1.0 - 2801 questions; 500 images.
[11 Feb 2021] test 1.0 - 3288 questions; 579 images.
[31 August 2023] updated to include question types in validation set.
- [Annotations](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazMvaW5mb2dyYXBoaWNzdnFhX3Fhcy56aXA=) (questions, answer, question types...)    
- [OCR](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazMvaW5mb2dyYXBoaWNzdnFhX29jci50YXIuZ3o=) (Amazon Textract)    
- [Images](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazMvaW5mb2dyYXBoaWNzdnFhX2ltYWdlcy50YXIuZ3o=)    
We also provide evaluation scripts so that participants can evaluate their methods in the exact same way as on the server.
- Infographics VQA [Evaluation scripts](https://rrc.cvc.uab.es/?com=downloads&action=download&ch=17&f=aHR0cHM6Ly9kYXRhc2V0cy5jdmMudWFiLmVzL3JyYy9Eb2NWUUEvVGFzazMlMjBldmFsdWF0aW9uJTIwc2NyaXB0LnppcA==)


#### Структура датасета

![](../files/Датасеты%20Полезные%20источники-20241120-10.png)


#### Примеры изображений

![](../files/Датасеты%20Полезные%20источники-20241120.png)







### [TextVQA dataset](https://textvqa.org/dataset/)  

Набор данных для оценки визуального мышления на основе текста в изображениях. TextVQA требует, чтобы модели читали и рассуждали о тексте в изображениях, чтобы отвечать на вопросы о них.
Первая версия 2019, вторая версия 2020.
Собран из другого датасета [OpenImages](https://storage.googleapis.com/openimages/web/download.html)
Ссылка на валидационную часть??
OCR токены извлечены с помощью [Rosetta](https://code.fb.com/ai-research/rosetta-understanding-text-in-images-and-videos-with-machine-learning/) (Meta AI)
[MMF (Multimodal Framework)](https://github.com/facebookresearch/mmf) - открытая платформа для разработки и обучения multimodal моделей (2019).

#### Структура датасета


![](../files/Датасеты%20Полезные%20источники-20241120-11.png)


- Вопрос-Ответ

![](../files/Датасеты%20Полезные%20источники-20241120-12.png)

- OCR разметка

![](../files/Датасеты%20Полезные%20источники-20241120-13.png)

#### Примеры изображений

![](../files/Датасеты%20Полезные%20источники-20241120-14.png)

#### Пояснения

**OCR tokens (Optical Character Recognition tokens)** - это единицы текста, которые получаются в результате распознавания оптических символов (OCR) на изображении или скане документа.

OCR tokens могут быть различными единицами текста, такими как:
- Символы (например, буквы, цифры, знаки препинания)    
- Слова    
- Фразы    
- Абзацы     

**Rosetta system** - это система машинного обучения для распознавания и перевода текста на изображениях и видео.
Поддерживает языки: английский, испанский, французский и другие.
Компоненты:
1. Модель распознавания текста (Text Recognition Model)    
2. Модель перевода текста (Text Translation Model)    
3. Модель классификации текста (Text Classification Model)    
  



### [RusTitW: Russian Language Visual Text Recognition](https://www.kaggle.com/datasets/hardtype/rustitw-russian-language-visual-text-recognition)

Есть реальные изображения с русским языком.
Подходит для теста чтения русского языка моделью VLLM.
Набор данных, размеченный человеком, для распознавания русского текста в реальных условиях.
С реальными данными намешаны сгенерированные.
Есть код для воспроизведения процесса генерации.
В данных есть дубликаты, отличающиеся только разрешением; картинки из трейна могут быть в тесте; есть картинки с английским текстом.
Синтетику делали с помощью [SynthText](https://github.com/markovivl/SynthText).

#### Структура датасета
![](../files/Датасеты%20Полезные%20источники-20241120-15.png)

- OCR разметка

![](../files/Датасеты%20Полезные%20источники-20241120-16.png)

>left - x-axis relative left position of bbox (x_min)
>top - y-axis relative top position of bbox (y_min)
>width - x-axis relative width of bbox
>height - y-axis relative height of bbox
>label - text inside bounding box
>shape - always 'rectangle'

#### Примеры изображений

![](../files/Датасеты%20Полезные%20источники-20241120-17.png)




  
  
  



### [InstructDoc](https://github.com/nttmdlab-nlp/instructdoc)

Датасет для решения задачи обобщения моделей на невиданные ранее задачи в области понимания визуальных документов (Visual Document Understanding, VDU). 
Включает 12 типов задач, основанных на 30 различных наборах данных, таких как визуальный вопрос-ответ, аннотирование, классификация документов и другие.

Как это работает:
- Инструкции как основа обучения:
В отличие от традиционных подходов, где модели обучаются на строго определённых задачах, в InstructDoc каждая задача описана с помощью инструкций. Инструкции включают описание намерения (что должно быть сделано) и стиль ответа (например, извлечение текста или генерация ответа).
- Архитектура модели InstructDr:
Модель использует модуль Document-former, который объединяет текстовые и визуальные признаки документа, преобразуя их в представления, которые можно обработать крупной языковой моделью (LLM).
Модель поддерживает многостраничные документы. 

Ограничения:
Текущая эффективность сильно зависит от качества распознавания текста (OCR) и не всегда учитывает сложные корреляции между различными текстами в документе. 

Сделали скрипты для скачивания [датасетов](https://github.com/nttmdlab-nlp/InstructDoc/tree/main/download_scripts)
  
![](../files/Датасеты%20Полезные%20источники-20241120-18.png)