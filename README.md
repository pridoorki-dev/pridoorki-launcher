<!--
  Репозиторий релизов / канала обновлений лаунчера.
  Сюда кладут: update.txt, update-history.txt, CHANGELOG.txt и Releases с установщиком.
  Исходники приложения — отдельно.
-->

<div align="center">

<br>

<img
  src="https://raw.githubusercontent.com/pridoorki-dev/pridoorki-launcher/main/assets/mark.png"
  alt="Pridoorki"
  width="96"
  onerror="this.style.display='none'"
/>

<h1>
  <span style="color:#1a1410">Pridoorki</span>
  <span style="color:#c99200">Launcher</span>
</h1>

<p>
  <em style="color:#5c5348;font-size:1.05em">
    Тёплый клиент для сборки Pridoorki — установка, обновления и синк контента в одном окне.
  </em>
</p>

<p>
  <a href="https://github.com/pridoorki-dev/pridoorki-launcher/releases/latest">
    <img
      src="https://img.shields.io/github/v/release/pridoorki-dev/pridoorki-launcher?style=for-the-badge&label=Скачать&labelColor=1a1410&color=e8b000&logo=windows&logoColor=fff"
      alt="Latest release"
    />
  </a>
  &nbsp;
  <a href="https://github.com/pridoorki-dev/pridoorki-launcher-pack-data">
    <img
      src="https://img.shields.io/badge/Сборка-pack--data-1a1410?style=for-the-badge&labelColor=f5e6b8&color=1a1410"
      alt="Pack data"
    />
  </a>
</p>

<br>

</div>

---

<table>
  <tr>
    <td width="55%" valign="top">

### Для игроков

Это **не исходники**, а канал дистрибуции:

1. Скачай последний установщик из
   <a href="https://github.com/pridoorki-dev/pridoorki-launcher/releases/latest"><strong>Releases</strong></a>
2. Установи и запусти **Pridoorki Launcher**
3. Лаунчер сам подтянет PineconeMC, профиль и серверную сборку

Ничего руками из этого репозитория копировать не нужно — только установщик.

    </td>
    <td width="45%" valign="top">

### Для админов

В корне ветки <code>main</code> лежат файлы, по которым клиент понимает,
есть ли обновление:

| Файл | Зачем |
|:-----|:------|
| <code>update.txt</code> | Версия, флаг mandatory, ссылка на exe |
| <code>update-history.txt</code> | История релизов (форс, если отстали) |
| <code>CHANGELOG.txt</code> | Текст в окне обновления |

    </td>
  </tr>
</table>

<br>

<div align="center">

### Как устроен канал обновлений

</div>

<pre style="background:#1a1410;color:#f5e6b8;padding:1.1em 1.25em;border-radius:12px;line-height:1.55">
pridoorki-launcher/
├── update.txt              ← latest: version / mandatory / download
├── update-history.txt      ← все релизы (mandatory / optional)
├── CHANGELOG.txt           ← что показать в окне
└── Releases/
    └── Pridoorki.Launcher_x.y.z_x64-setup.exe
</pre>

<details>
<summary><strong>Пример <code>update.txt</code></strong></summary>
<br>

```text
version: 0.2.5
mandatory: false
download: https://github.com/pridoorki-dev/pridoorki-launcher/releases/download/v0.2.5/Pridoorki.Launcher_0.2.5_x64-setup.exe
```

- <code>version</code> — сравнивается с версией в приложении  
- <code>mandatory</code> — <code>true</code> / <code>yes</code> / <code>да</code> → без кнопки «Позже»  
- <code>download</code> — прямая ссылка; если нет — берётся <code>.exe</code> из latest Release  

</details>

<details>
<summary><strong>Пример <code>update-history.txt</code></strong></summary>
<br>

```text
# Новые сверху удобнее читать; порядок для клиента не важен.
0.2.5
0.2.4 mandatory
0.2.3
0.2.2
```

Клиент делает обновление **обязательным**, если:

1. между установленной и latest есть хотя бы один <code>mandatory</code>, **или**
2. отставание **≥ 2** релизов из этого списка  

Нет файла → учитывается только флаг из <code>update.txt</code>.

</details>

<details>
<summary><strong>Пример <code>CHANGELOG.txt</code></strong></summary>
<br>

```text
• Быстрее ставятся отдельные моды
• Понятнее сообщения про GitHub API
• Счётчик файлов n / всего при синке
```

</details>

<br>

<div align="center">

### Что умеет лаунчер

</div>

<table>
  <tr>
    <td align="center" width="33%">
      <h3>PineconeMC</h3>
      <p>Ставит и ведёт portable-профиль,<br>без ручной возни с путями.</p>
    </td>
    <td align="center" width="33%">
      <h3>Синк сборки</h3>
      <p>Тянет моды и опциональный контент<br>из <a href="https://github.com/pridoorki-dev/pridoorki-launcher-pack-data">pack-data</a>.</p>
    </td>
    <td align="center" width="33%">
      <h3>Обновления</h3>
      <p>Сам замечает новую версию<br>и предлагает установщик.</p>
    </td>
  </tr>
</table>

<br>

---

<div align="center">

<p style="color:#5c5348">
  Сделано для сервера <strong style="color:#1a1410">Pridoorki</strong>
  · Windows x64
  · <a href="https://github.com/pridoorki-dev/pridoorki-launcher-pack-data">репозиторий сборки →</a>
</p>

<p>
  <sub style="color:#8a8074">
    Если картинка-марка сверху не загрузилась — просто положи логотип в
    <code>assets/mark.png</code> этого репо или убери блок <code>&lt;img&gt;</code>.
  </sub>
</p>

</div>
