# Описание

* Проект содержит шаблон для распределенной работы команды с `Obsidian`([ссылка](https://obsidian.md/download)).
* Позволяет организовать распределенную Базу знаний (Вики) для команды.
* Из него может быть развернут публичный статический сайт.

Например на платформе `GitHub Pages`([ссылка](https://pages.github.com/)).
Благодаря этому, можно так же работать над документацией по своему проекту, используя возможности `Obsidian`([ссылка](https://obsidian.md/download)).

# Настройка

1. Скачайте и установите `Obsidian`([ссылка](https://obsidian.md/download)) для свой ОС и установите его.
2. Клонируйте себе данный репозиторий.
Выберите желаемую папку, и внутри нее в терминале выполните команду:
```
git clone git@github.com:medphisiker/multimodal_models_for_docs_wiki.git
```

Настройте свое `имя` и `email` для данного git-репозитория, выполнив команду:
```
git config --local user.name "YourName YouSurname"
git config --local user.email "your@email.adress"
```

Эта директория станет хранилищем для всех файлов и настроек `Obsidian`, она станет его `Vault`.

Далее будем называть эту папку `Obsidian Git Vault`.

3. Скачайте архив `template_obisdian_cfg.zip` из Google Drive папки [ссылка](https://drive.google.com/drive/folders/1GLPKjVHtxfcPXCeAq-5XCx_nXHbsejiy?usp=sharing).
4. Распакуйте скаченный архив внутри папки `Obsidian Git Vault`.
5. Проверьте полученную структуру каталога `Obsidian Git Vault`.

Она должна выглядеть так:
```
├───.obsidian
│   └───plugins
│       ├───better-export-pdf
│       ├───image-captions
│       ├───obsidian-excalidraw-plugin
│       ├───obsidian-paste-image-rename
│       ├───oz-clear-unused-images
│       └───tag-wrangler
├───cards
├───files
│   └───Excalidraw
│       └───Scripts
│           └───Downloaded
├───projects
├───repo_pics
└───templates
```

Для этого на `Windows` можно открыть `cmd`-терминал, на `Linux/Unix` их терминал внутри папки `Obsidian Git Vault` и выполнить команду:
```
tree
```

# 6. Выбираем в программе `Obsidian` в качестве нашего хранилища папку `Obsidian Git Vault`.

## Шаг 1 Запускаем программу `Obsidian`

Если у Вы уже используете `Obsidian`, он откроет ваше личное хранилище.

Вам нужно будет переключится на хранилище указав нашу папку `Obsidian Git Vault`.

![manage_vaults](../repo_pics/manage_vaults.jpg)

Если программы `Obsidian` ранее не было у вас на ПК она сама при своем первом запуске предложит Вам выбрать папку для хранилища.
## Шаг 2 Выбираем папку `Obsidian Git Vault` как хранилище

![chose_your_vault_1](../repo_pics/chose_your_vault_1.jpg)


![chose_your_vault_2](../repo_pics/chose_your_vault_2.jpg)
## Шаг 3 Доверится автору и включить плагины

После выбора папки `Obsidian Git Vault` в качестве хранилища для заметок, появится окно.

Оно сообщит Вам, что данное хранилище использует набор сторонних плагинов для `Obsidian`.

Так и было задумано, они были в архиве `template_obisdian_cfg.zip`, который мы распаковывали ранее.

Соглашаемся с активацией сторонних плагинов внутри нашего хранилища.

![Trust_the_author_and_enable_plugins](../repo_pics/Trust_the_author_and_enable_plugins.jpg)
## Шаг 4 Настраиваем Git

> За этот шаг выражаем благодарность Юлии ([ссылка на профиль GitHub](https://github.com/YuliaOv22))

* Кажется это нюанс работы `Obsidian` на `Windows`, но это не точно.
* Лучше сделать эту настройку на всех ОС.

После открытия `Markdown`-файлов заметок в `Obsisidian`, даже если содержание заметок не было изменено, `git` будет показывать нам, что `Markdown`-файл был изменен.
При этом он не сможет отобразить изменения в содержании файла потому, что их нет.

Отредактируем настройки `git` так, чтобы он показывал нам в качестве измененных файлов только те заметки, содержание, которых было действительно изменено ([ссылка на источник](https://forum.obsidian.md/t/workaround-for-rendering-markdown-files-on-windows-results-in-timestamp-changes-detected-by-git/53039/4)).

Для этого можно использовать команды `git` в терминале, но они немного отличаются для разных версий `git`. Наиболее универсальный способ, отредактировать файл настроек `git` внутри нашего репозитория вручную.

Для этого в каталоге нашего репозитория `Obsidian Git Vault` откроем файл `.git/config`.
Открывать лучше редактором, который отображает все спец. символы, например, `Notepad++` или вашей любимой `IDE`.
Добавим в раздел `[core]` такие строки:

```
[core]
	bare = false
	autocrlf = false
	trustctime = false
	[core]
```

> У разных версий `git` будут отличаться знаки разделителя блоков в форматировании файла `.git/config`.
> При редактировании опирайтесь формат на вашего файла `.git/config`.

После этого нужно будет перезапустить `git`, чтобы наши изменения локальных настроек `git` (на уровне данного репозитория) вступили в силу.
Можно выполнить специальные команды в терминале, которые будут немного отличаться для разных версий `git` и ОС или поступить более простым и универсальным способом - перезагрузить ОС.
## Шаг 5 Используем распределенную базу знаний

1. Используем `Obsidian`, чтобы создавать заметки в формате `Markdown`-файлов.

* Синтаксис Markdown: подробная шпаргалка для веб-разработчиков [ссылка](https://skillbox.ru/media/code/yazyk-razmetki-markdown-shpargalka-po-sintaksisu-s-primerami/)
* Курс по Obsidian [ссылка](https://youtube.com/playlist?list=PLeDR6lYFEHWEUxwSA8OplPLvk50DCVraH&si=vjNqi9xUT_rSRp74)
* An Introduction to Obsidian Properties [ссылка](https://obsidian.rocks/an-introduction-to-obsidian-properties/)
* How to Make a Template in Obsidian [ссылка](https://www.alphr.com/obsidian-how-to-make-a-template/)

2. Используем плагины `Obsidian`, которые мы активировали:

* **Excalidraw** ([ссылка](https://github.com/zsviczian/obsidian-excalidraw-plugin?tab=readme-ov-file)) - крутой плагин для создания диаграмм, редактирования картинок и т.д.

Можно использовать вместо Miro совместно всеми участниками проекта =)

Базовый набор его возможностей:
* Obsidian-Excalidraw 1.2.0 Walkthrough Part 1/10 (смотрим все 10 штук) [ссылка на 1 видео](https://youtu.be/sY4FoflGaiM?si=LUziSDrIEGsOEytF)
* YouTube Канал автора плагина [ссылка](https://www.youtube.com/@VisualPKM/playlists)
* Онлайн сервис Excalidraw на взаимодействии с которым построен плагин [ссылка](https://www.youtube.com/@VisualPKM/playlists)

Будем в нем рисовать красивые схемы/диаграммы/брейнштормить и т.д.

* **Better Export PDF** - позволяет экспортировать заметки в pdf файлы. Exalidraw - диаграммы будут преобразованы в картинки
* **Image Captions** - позволяет делать подписи рисункам
* **Paste image rename** - автоматически переименовывает картинки, которые мы вставляем в имя заметки.
* **Clear Unused Images** - перемещает все неиспользуемые картинки в корзину.

Использовать осторожно, плагины от `Exalidraw` он тоже стремится удалить.
