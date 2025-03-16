# MangaStatus

**MangaStatus** — это приложение для отображения настраиваемого статуса в Discord. Вы можете настроить активность, добавить кнопки с ссылками, указать количество участников в группе и многое другое.

## Скачать

Последняя версия доступна в разделе [Releases](https://github.com/SPIDIKSY/MangaStatus/releases).  
Скачайте файл `MangaStatus.exe` и запустите его — никаких дополнительных установок не требуется!

## Установка для новичков

Если вы впервые используете MangaStatus, следуйте этим простым шагам:

1. **Скачайте приложение**:
   - Перейдите в раздел [Releases](https://github.com/SPIDIKSY/MangaStatus/releases).
   - Найдите релиз с названием `MangaStatus v1.0 - First Release`.
   - Скачайте файл `MangaStatus.exe`, нажав на его название.
   - Сохраните файл в удобное место, например, на рабочий стол.

2. **Запустите приложение**:
   - Дважды щёлкните по файлу `MangaStatus.exe`.
   - Если антивирус или Windows покажет предупреждение, нажмите "Разрешить" или "Запустить всё равно" (это ложное срабатывание, так как файл создан с помощью PyInstaller).

3. **Настройте статус**:
   - Введите `Client ID` (см. раздел "Описание полей" ниже, чтобы узнать, как его получить).
   - Заполните другие поля (например, `Details`, `State`, кнопки и т.д.).
   - Нажмите на кнопку ▶ (зелёная кнопка "Подключиться") для запуска статуса в Discord.

## Описание полей программы

MangaStatus содержит несколько полей для настройки статуса в Discord. Вот подробное описание каждого поля и инструкции, откуда взять необходимые данные:

### 1. Client ID
- **Описание**: Уникальный идентификатор вашего приложения в Discord. Без него программа не сможет подключиться к Discord.
- **Откуда взять**:
  1. Перейдите на сайт [Discord Developer Portal](https://discord.com/developers/applications).
  2. Нажмите **New Application** и дайте имя вашему приложению (например, "MangaStatus").
  3. На странице приложения в разделе **General Information** найдите поле **Application ID** — это и есть ваш `Client ID`.
  4. Скопируйте его и вставьте в поле `Client ID` в MangaStatus.
- **Совет**: Отметьте галочку "Сохранить" рядом с полем, чтобы не вводить `Client ID` каждый раз.

### 2. Тип активности
- **Описание**: Задаёт тип активности, который отображается в верхней строке статуса в Discord (например, "Играет в", "Слушает", "Смотрит").
- **Варианты**:
  - Играет в
  - Слушает
  - Смотрит
  - Стримит
  - Соревнуется в
- **Откуда взять**: Просто выберите нужный тип из выпадающего списка.

### 3. Details
- **Описание**: Основная строка статуса, которая описывает вашу активность (например, название игры, песни или видео).
- **Пример**: Если вы выбрали "Слушает" в "Тип активности" и ввели "Музыка" в `Details`, в Discord отобразится "Слушает: Музыка".
- **Откуда взять**: Введите любое описание, которое хотите показать в статусе.

### 4. State
- **Описание**: Дополнительная информация о статусе, которая отображается ниже строки `Details`.
- **Пример**: Если вы указали "Уровень 10", в статусе Discord это будет отображаться как вторая строка.
- **Откуда взять**: Введите любую дополнительную информацию (например, уровень, исполнитель песни, эпизод видео).

### 5. Large Image Key
- **Описание**: Ключ большого изображения, которое отображается в статусе.
- **Откуда взять**:
  1. В Discord Developer Portal в вашем приложении перейдите в раздел **Rich Presence** → **Art Assets**.
  2. Загрузите изображение (например, логотип или обложку).
  3. После загрузки вы увидите ключ изображения (например, `large_icon`). Скопируйте его и вставьте в это поле.
- **Совет**: Размер изображения должен быть 1024x1024 пикселя для лучшего качества.

### 6. Small Image Key
- **Описание**: Ключ малого изображения, которое отображается в углу большого изображения.
- **Откуда взять**: Аналогично `Large Image Key`, загрузите второе изображение в **Art Assets** и скопируйте его ключ.
- **Совет**: Малое изображение обычно меньше, например, 128x128 пикселей.

### 7. Кнопка 1 - Текст и URL / Кнопка 2 - Текст и URL
- **Описание**: Позволяет добавить до двух кнопок в статус, которые ведут на внешние ссылки (например, на сайт или Discord-сервер).
- **Поля**:
  - **Текст**: Название кнопки (максимум 32 символа). Например, "Мой сайт" или "Мой Discord".
  - **URL**: Ссылка, на которую ведёт кнопка. Например, `https://example.com` или `https://discord.com`.
- **Откуда взять**:
  - Текст: Придумайте название кнопки (например, "Присоединиться").
  - URL: Вставьте ссылку на ваш сайт, Discord-сервер или любую другую страницу.

### 8. Party (Size и Max)
- **Описание**: Отображает количество участников в группе (например, для игр или совместных активностей).
- **Поля**:
  - **Size**: Текущее количество участников (должно быть меньше или равно `Max`).
  - **Max**: Максимальное количество участников.
- **Пример**: Если `Size` = 3 и `Max` = 5, в статусе отобразится "3/5".
- **Откуда взять**: Введите числа, соответствующие вашей группе (например, `Size` = 2, `Max` = 4).

## Поддержка

Если у вас есть вопросы, предложения или вы хотите поддержать проект:

- **Boosty**: [Поддержать на Boosty](https://boosty.to/spidiksy)
- **Telegram**: [t.me/spidvrassrochku](https://t.me/spidvrassrochku)
- **Discord**: @spidiksy

## Лицензия

Все права принадлежат SPIDIKSY. Запрещена декомпиляция и распространение без риска лишиться правого яичка.
