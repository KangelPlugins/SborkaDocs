# RU:

---

Файл сборки `.kpm` — это JSON-конфигурация, описывающая набор плагинов для установки через KPM **(Kangel Plugins Manager)**
Сборка позволяет:

* быстро устанавливать набор плагинов
* делиться готовыми конфигурациями
* стандартизировать наборы под задачи (UI, NSFW, утилиты и т.д.)

---

## 📄 Структура файла

Пример:

```json
{
    "metadata": {
        "name": "My Pack",
        "author": "username",
        "description": "Описание сборки",
        "icon": "pack_name/0"
    },
    "plugins": [
        "tg://kpm_install?plugin=example_plugin"
    ],
    "format": "kpm_collection_v2"
}
```

---

## 🔑 Поля

### 1. `format` (обязательное)

```json
"format": "kpm_collection_v2"
```

* Константа
* Всегда должна быть `"kpm_collection_v2"`
* Используется для определения версии формата

---

### 2. `metadata` (обязательное)

```json
"metadata": {
    "name": "Название сборки",
    "author": "Автор",
    "description": "Описание",
    "icon": "pack_name/index"
}
```

#### Поля:

| Поле          | Тип    | Описание                                  |
| ------------- | ------ | ----------------------------------------- |
| `name`        | string | Название сборки                           |
| `author`      | string | Автор (ник/имя)                           |
| `description` | string | Краткое описание                          |
| `icon`        | string | Иконка сборки в формате `pack_name/index` |

📌 Рекомендации:

* `name` — короткий и понятный
* `description` — что делает сборка (например: "UI + утилиты + фан")
* `icon` — валидный стикерпак и индекс

---

### 3. `plugins` (обязательное)

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre"
]
```

Массив ссылок на плагины
(**берутся из магазина KPM + сюда обязательно добавляй все зависимости**)

#### Пример:

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre",
    "tg://kpm_install?plugin=Unlimited_GIFs",
    "tg://kpm_install?plugin=fake_stars"
]
```

---

## ⚠️ Особенности `icon`

* Формат строго:

  ```text
  pack_name/index
  ```
* Стикерпак должен существовать
* Индекс не должен выходить за пределы
* Если поле отсутствует — используется дефолтная иконка
* При ошибке формат просто игнорируется (иконка не отобразится)

---

## 🧪 Пример нормальной сборки

```json
{
    "metadata": {
        "name": "Ultimate Pack",
        "author": "mandre",
        "description": "UI + полезные утилиты + фан плагины",
        "icon": "kangel_pack/5"
    },
    "plugins": [
        "tg://kpm_install?plugin=ReMandre",
        "tg://kpm_install?plugin=Unlimited_GIFs",
        "tg://kpm_install?plugin=fake_stars",
        "tg://kpm_install?plugin=favstickers",
        "tg://kpm_install?plugin=lastfm",
        "tg://kpm_install?plugin=log_overlay"
    ],
    "format": "kpm_collection_v2"
}
```

---

# EN:

---

A `.kpm` build file is a JSON configuration that defines a set of plugins for installation via KPM **(Kangel Plugins Manager)**.

Builds allow you to:

* quickly install a set of plugins
* share ready-to-use configurations
* standardize setups for specific purposes (UI, NSFW, utilities, etc.)

---

## 📄 File Structure

Example:

```json
{
    "metadata": {
        "name": "My Pack",
        "author": "username",
        "description": "Build description",
        "icon": "pack_name/0"
    },
    "plugins": [
        "tg://kpm_install?plugin=example_plugin"
    ],
    "format": "kpm_collection_v2"
}
```

---

## 🔑 Fields

### 1. `format` (required)

```json
"format": "kpm_collection_v2"
```

* Constant value
* Must always be `"kpm_collection_v2"`
* Used to determine the format version

---

### 2. `metadata` (required)

```json
"metadata": {
    "name": "Build name",
    "author": "Author",
    "description": "Description",
    "icon": "pack_name/index"
}
```

#### Fields:

| Field         | Type   | Description                            |
| ------------- | ------ | -------------------------------------- |
| `name`        | string | Build name                             |
| `author`      | string | Author (nickname/name)                 |
| `description` | string | Short description                      |
| `icon`        | string | Build icon in `pack_name/index` format |

📌 Recommendations:

* `name` — keep it short and clear
* `description` — explain what the build includes
* `icon` — must point to a valid sticker pack and index

---

### 3. `plugins` (required)

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre"
]
```

An array of plugin links
(**taken from the KPM store + you must include all dependencies here as well**)

#### Example:

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre",
    "tg://kpm_install?plugin=Unlimited_GIFs",
    "tg://kpm_install?plugin=fake_stars"
]
```

---

## ⚠️ `icon` notes

* Strict format:

  ```text
  pack_name/index
  ```
* Sticker pack must exist
* Index must be valid
* If not provided — default icon is used
* Invalid format → icon will not be displayed

---

## 🧪 Example of a valid build

```json
{
    "metadata": {
        "name": "Ultimate Pack",
        "author": "mandre",
        "description": "UI + useful utilities + fun plugins",
        "icon": "kangel_pack/5"
    },
    "plugins": [
        "tg://kpm_install?plugin=ReMandre",
        "tg://kpm_install?plugin=Unlimited_GIFs",
        "tg://kpm_install?plugin=fake_stars",
        "tg://kpm_install?plugin=favstickers",
        "tg://kpm_install?plugin=lastfm",
        "tg://kpm_install?plugin=log_overlay"
    ],
    "format": "kpm_collection_v2"
}
```

---

