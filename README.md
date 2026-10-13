<div align="center">

# 🐉 WYVERN

**Клиентский мод для Minecraft на базе Fabric** —
модульная система, кастомный рендер-движок, HUD и GUI.

[![Minecraft](https://img.shields.io/badge/Minecraft-1.21.4-62B47A?style=for-the-badge&logo=minecraft&logoColor=white)](https://minecraft.net)
[![Fabric Loader](https://img.shields.io/badge/Fabric_Loader-0.16.10+-D8A657?style=for-the-badge&logo=fabric&logoColor=white)](https://fabricmc.net)
[![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org)
[![Gradle](https://img.shields.io/badge/Gradle-8.14.1-02303A?style=for-the-badge&logo=gradle&logoColor=white)](https://gradle.org)

*370 классов · 76 модулей · 45 миксинов · 118 ресурсов*

</div>

---

## ✨ Что внутри

| | |
|---|---|
| 🧩 **Модульная система** | 76 модулей с настройками (слайдеры, режимы, цвета) в 5 категориях |
| ⚔️ **Combat / Movement / Player** | 32 игровых модуля: CrystalAura, AutoTotem, ротации, элитра-механики, предсказания |
| 🌈 **Render** | 30 визуальных модулей — ESP, кастомное небо, эффекты убийств, косметика, шейдеры рук |
| 🎨 **Рендер-движок** | 20+ шейдеров (Kawase-blur, bloom, градиенты, squircle, metanoise), частицы, 2D/3D утилиты |
| 🔤 **MSDF-шрифты** | Векторный рендер текста через MSDF-атласы — чётко на любом масштабе |
| 🖥️ **HUD и GUI** | Перетаскиваемые HUD-элементы, меню клиента, темы (`ThemeManager`), анимации с easing |
| 💬 **Discord RPC** | Rich Presence с callback'ами (join / spectate / ready) и нативным `discord-rpc.dll` |
| 🔧 **Инфраструктура** | Команды, конфиги, макросы, скрипты, автобайт, вейпоинты, событийная шина |

## 🧭 Модули по категориям

| Категория | Модулей | Описание |
|---|:---:|---|
| `render` | 30 | ESP, эффекты, косметика, визуальные улучшения |
| `misc` | 14 | утилиты и прочие удобства |
| `combat` | 12 | боевая механика (+15 классов ротаций) |
| `movement` | 11 | передвижение и физика |
| `player` | 9 | взаимодействие игрока с миром |

## 🗂 Структура проекта

```
wywern/
├── src/main/
│   ├── java/
│   │   ├── wtf/wyvern/                  # основной код мода
│   │   │   ├── Wyvern.java              # точка входа (ClientModInitializer)
│   │   │   ├── base/                    # ядро клиента
│   │   │   │   ├── modules/             #   ModuleManager
│   │   │   │   ├── comand/              #   команды и аргументы
│   │   │   │   ├── config/              #   конфиги
│   │   │   │   ├── discord/             #   Discord Rich Presence
│   │   │   │   ├── events/              #   события (input, player, render, server)
│   │   │   │   ├── font/                #   MSDF-рендер шрифтов
│   │   │   │   ├── theme/               #   темы оформления
│   │   │   │   └── …                    #   autobuy, macro, notify, waypoint, request
│   │   │   ├── client/                  # клиентская часть
│   │   │   │   ├── modules/impl/        #   76 модулей в 5 категориях
│   │   │   │   ├── hud/elements/        #   HUD-элементы и уведомления
│   │   │   │   └── screens/menu/        #   меню клиента
│   │   │   └── utility/                 # утилиты
│   │   │       ├── mixin/               #   45 миксинов + accessors
│   │   │       ├── render/              #   display (2D), level (3D), particles, shaders
│   │   │       ├── game/                #   combat, player, server
│   │   │       └── …                    #   math, predict, crypt, interfaces
│   │   ├── ru/nexusguard/               # protection / аннотации
│   │   └── com/darkmagician6/           # event API
│   └── resources/
│       ├── fabric.mod.json              # манифест мода
│       ├── wyvern.mixins.json           # конфиг миксинов
│       ├── wyvern.accesswidener
│       └── assets/wyvern/               # шейдеры, MSDF-шрифты, иконки, звуки
├── build.gradle
├── gradle.properties                    # версии Minecraft / Fabric / API
└── gradle/wrapper/                      # Gradle 8.14.1
```

## 🚀 Запуск

**Требования:** JDK 21+

```bash
# клонировать
git clone https://github.com/poctupkosasa-maker/wywern.git
cd wywern

# запустить клиент с модом (разработка)
./gradlew runClient

# собрать jar (появится в build/libs/)
./gradlew build
```

> Первая сборка скачает Minecraft и зависимости через Fabric Loom —
> это может занять несколько минут.

## ⚙️ Технический стек

| Компонент | Версия |
|---|---|
| Minecraft | 1.21.4 |
| Fabric Loader | 0.16.10 |
| Fabric API | 0.119.3+1.21.4 |
| Fabric Loom | 1.10 |
| Gradle | 8.14.1 |
| Java | 21 |
| Lombok | 1.18.38 |

---

<div align="center">

*⚠️ All rights reserved.*
*Wyvern · 2026*

</div>
