<div align="center">

<img src="assets/mark.png" alt="Pridoorki" width="120" />

# Pridoorki Launcher

**Скачал — установил — играешь.**  
Один лаунчер для нашего сервера: сам поставит нужное, подтянет моды и подскажет, когда вышла новая версия.

[![Скачать](https://img.shields.io/github/v/release/pridoorki-dev/pridoorki-launcher?style=for-the-badge&label=%D0%A1%D0%BA%D0%B0%D1%87%D0%B0%D1%82%D1%8C&labelColor=1a1410&color=e8b000&logo=windows&logoColor=fff)](https://github.com/pridoorki-dev/pridoorki-launcher/releases/latest)

</div>

---

## Как начать

1. Открой [последний релиз](https://github.com/pridoorki-dev/pridoorki-launcher/releases/latest)
2. Скачай установщик (`…setup.exe`) и поставь как обычную программу
3. Запусти **Pridoorki Launcher** и нажми «Играть»

Дальше лаунчер сам разберётся: клиент, профиль, сборка с сервера. Из этой страницы ничего вручную копировать не нужно.

> Windows, 64-bit. Если антивирус ругается на новый установщик — это бывает у небольших программ; файл мы выкладываем сами.

---

## Что он делает

- **Ставит игру «как надо»** — без ручных путей и танцев с папками  
- **Держит сборку актуальной** — недостающие моды докачает сам  
- **Говорит про обновления** — если вышла новая версия лаунчера, предложит поставить  

Модпак живёт отдельно: [pridoorki-launcher-pack-data](https://github.com/pridoorki-dev/pridoorki-launcher-pack-data).

---

## Картинки на этой странице

Уже лежат рядом с README — просто залей папку `assets/` в корень репозитория вместе с этим файлом:

```text
pridoorki-launcher/
├── README.md
├── assets/
│   ├── mark.png          ← логотип сверху (из static/pridoorki.png)
│   ├── icon.png          ← иконка приложения (из src-tauri/icons/icon.png)
│   └── banner-logo.png   ← запасной логотип (logo_doorki.png)
├── update.txt
├── update-history.txt
├── CHANGELOG.txt
└── (релизы с установщиком — во вкладке Releases)
```

Откуда взять, если потеряешь:

| Файл | Откуда в проекте лаунчера |
|------|---------------------------|
| `assets/mark.png` | `static/pridoorki.png` |
| `assets/icon.png` | `src-tauri/icons/icon.png` |
| `assets/banner-logo.png` | `static/logo_doorki.png` |

В README картинка подключается так: `![…](assets/mark.png)` — относительный путь, без raw.githubusercontent, пока файлы не залиты.

---

<details>
<summary>Для тех, кто выкладывает обновления лаунчера</summary>

<br>

В корне ветки `main` три текстовых файла — по ним лаунчер понимает, что пора обновляться.

**`update.txt`** — что считать «последней» версией:

```text
version: 0.2.5
mandatory: false
download: https://github.com/pridoorki-dev/pridoorki-launcher/releases/download/v0.2.5/Pridoorki.Launcher_0.2.5_x64-setup.exe
```

**`update-history.txt`** — список релизов (чтобы догнать тех, кто далеко отстал):

```text
0.2.5
0.2.4 mandatory
0.2.3
```

**`CHANGELOG.txt`** — короткий текст «что нового» в окошке обновления.

Установщик клади в **Releases**, не в дерево файлов репозитория.

</details>

---

<div align="center">

Сделано с теплом для **Pridoorki** · только Windows x64

[Сборка модов →](https://github.com/pridoorki-dev/pridoorki-launcher-pack-data)

</div>
