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
        "description": "Описание сборки"
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
    "description": "Описание"
}
```

#### Поля:

| Поле          | Тип    | Описание         |
| ------------- | ------ | ---------------- |
| `name`        | string | Название сборки  |
| `author`      | string | Автор (ник/имя)  |
| `description` | string | Краткое описание |

📌 Рекомендации:

* `name` — короткий и понятный
* `description` — что делает сборка (например: "UI + утилиты + фан")

---

### 3. `plugins` (обязательное)

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre"
]
```
Массив ссылок на плагины (БЕРУТСЯ ИЗ МАГАЗИНА KPM + ТУДА ПРОПИСЫВАЙ ВСЕ ЗАВИСИОМСТИ ТАКЖЕ) 

#### Пример:

```json
"plugins": [
    "tg://kpm_install?plugin=ReMandre",
    "tg://kpm_install?plugin=Unlimited_GIFs",
    "tg://kpm_install?plugin=fake_stars"
]
```


## 🧪 Пример нормальной сборки

```json
{
    "metadata": {
        "name": "Ultimate Pack",
        "author": "mandre",
        "description": "UI + полезные утилиты + фан плагины"
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
        "description": "Build description"
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
    "description": "Description"
}
```

#### Fields:

| Field         | Type   | Description            |
| ------------- | ------ | ---------------------- |
| `name`        | string | Build name             |
| `author`      | string | Author (nickname/name) |
| `description` | string | Short description      |

📌 Recommendations:

* `name` — keep it short and clear
* `description` — explain what the build includes (e.g. "UI + utilities + fun")

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

## 🧪 Example of a valid build

```json
{
    "metadata": {
        "name": "Ultimate Pack",
        "author": "mandre",
        "description": "UI + useful utilities + fun plugins"
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



