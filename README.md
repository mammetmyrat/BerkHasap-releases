<div align="center">

<img src="https://raw.githubusercontent.com/mammetmyrat/BerkHasap-releases/main/assets/logo.png" alt="BerkHasap" width="120">

# BerkHasap

**Автономная касса и складской учёт для магазина**
Работает без интернета · Русский · Türkmençe · English

[![Версия](https://img.shields.io/github/v/release/mammetmyrat/BerkHasap-releases?label=версия&color=005145&style=for-the-badge)](https://github.com/mammetmyrat/BerkHasap-releases/releases/latest)
[![Скачиваний](https://img.shields.io/github/downloads/mammetmyrat/BerkHasap-releases/total?label=скачиваний&color=0A746C&style=for-the-badge)](https://github.com/mammetmyrat/BerkHasap-releases/releases)
![Платформы](https://img.shields.io/badge/Windows%20·%20macOS%20·%20Linux-3FA796?style=for-the-badge)

### [⬇️ Скачать последнюю версию](https://github.com/mammetmyrat/BerkHasap-releases/releases/latest)

</div>

---

## Что это

BerkHasap — программа для небольшого магазина: **касса, товары, склад, клиенты с долгами и отчёты** в одном окне.
Всё хранится на вашем компьютере, интернет нужен только для скачивания новых версий.

<!-- Добавьте скриншоты в папку assets/ и раскомментируйте:
<p align="center">
  <img src="assets/pos.png" width="49%" alt="Касса">
  <img src="assets/reports.png" width="49%" alt="Отчёты">
</p>
-->

## Возможности

| | |
|---|---|
| 🛒 **Касса** | Поиск по названию и штрихкоду (работает со сканером), розница и опт, оплата наличными, картой, смешанная и **в долг**, быстрые суммы и сдача, печать чека, возвраты и отмена продаж |
| 👥 **Клиенты и долги** | База клиентов, долги и предоплата, приём оплат, история покупок и оплат, баланс на чеке |
| 📦 **Товары и склад** | Каталог с категориями, приход, списание и корректировка остатков, порог «мало», история движения |
| 📊 **Отчёты** | Выручка и график по дням, топ товаров, маржа, остатки, должники и лучшие клиенты, экспорт в CSV |
| 💱 **Валюта** | Цены в TMT или в USD с автоматическим пересчётом по курсу |
| 👤 **Пользователи** | Администратор и кассиры с разными правами |
| 🧾 **Чек** | Название магазина, телефон, адрес, язык чека, предпросмотр |
| 💾 **Бэкап** | Автоматическая ежедневная копия базы и копия перед каждым обновлением |

**Горячие клавиши в кассе:** `F2` — поиск · `F3` — клиент · `F9` — оплата.

## Установка

Скачайте файл для вашей системы на странице [**Releases**](https://github.com/mammetmyrat/BerkHasap-releases/releases/latest).

### 🪟 Windows
1. Скачайте `BerkHasap-<версия>-windows.msi` и запустите его.
2. Если Windows показывает «Система Windows защитила ваш компьютер» — нажмите **Подробнее → Выполнить в любом случае**.
   (Программа пока без цифровой подписи — это нормально.)
3. Запустите **BerkHasap** из меню «Пуск».

### 🍎 macOS (Apple Silicon)
1. Скачайте `BerkHasap-<версия>-macos.dmg`, откройте и перетащите **BerkHasap** в «Программы».
2. При первом запуске macOS напишет, что не может проверить программу. Нажмите **Готово** (не «Переместить в корзину») и откройте
   **Системные настройки → Конфиденциальность и безопасность → Всё равно открыть**.
   Или одной командой в Терминале:
   ```bash
   xattr -dr com.apple.quarantine /Applications/BerkHasap.app
   ```

### 🐧 Linux (Debian / Ubuntu)
```bash
sudo apt install ./BerkHasap-<версия>-linux.deb
```

## Первый запуск

1. Войдите как администратор. Данные для первого входа вам сообщит поставщик — **сразу смените пароль**
   в *Настройки → Пользователи*.
2. Мастер первой настройки спросит название магазина, режим цен и курс, предложит создать кассира.
3. Добавьте первый товар в разделе **Каталог** — и можно продавать.
4. **Лицензия:** *Настройки → Лицензия* — скопируйте Machine ID и отправьте поставщику, чтобы получить ключ.

## Обновления

Программа сама проверяет новые версии при запуске. Если версия вышла, сверху появится баннер
**«Доступна новая версия»** с кнопкой **Скачать**. Установите новый файл **поверх** старой версии.

- ✅ Ваши данные (товары, продажи, клиенты, настройки) **сохраняются**.
- ✅ Лицензия остаётся активной.
- ✅ Перед первым запуском новой версии автоматически создаётся копия базы
  (`backups/pre-update-…`), чтобы всегда можно было вернуться.

Проверить вручную: *Настройки → О программе → Проверить обновления*.

## Где хранятся данные

Папка `.berkhasap` в вашей домашней папке:

| Что | Где |
|---|---|
| База данных | `.berkhasap/berkhasap.db` |
| Резервные копии | `.berkhasap/backups/` |
| Экспорт отчётов | `.berkhasap/exports/` |

Чтобы перенести программу на другой компьютер, скопируйте базу из бэкапа и восстановите её в
*Настройки → Бэкап → Восстановить*. Лицензия переносится отдельно — см. *Настройки → Лицензия*.

## Системные требования

- Windows 10/11 · macOS 12+ (Apple Silicon) · Ubuntu 22.04+ / Debian 12+
- 4 ГБ ОЗУ, ~400 МБ свободного места
- Экран от 1100×700

## Поддержка

Если что-то не работает или нужна лицензия — напишите:

- 📞 **+993 71 49 89 97**
- ✈️ **Telegram:** [@berkhasap](https://t.me/berkhasap)

При обращении укажите версию программы (*Настройки → О программе*) и, если можно, пришлите скриншот.

---

<details>
<summary><b>English</b></summary>

**BerkHasap** is an offline point-of-sale and inventory app for small shops: POS (cash / card / split / on credit),
products and stock, customers with debts and prepayments, reports with charts and CSV export.
Interface languages: Russian, Turkmen, English. Data stays on your computer.

**Install:** download the installer for your OS from the [latest release](https://github.com/mammetmyrat/BerkHasap-releases/releases/latest)
(`.msi` for Windows, `.dmg` for macOS on Apple Silicon, `.deb` for Linux). The installers are not signed yet, so Windows
SmartScreen / macOS Gatekeeper will ask you to confirm the first launch.
**Updates:** the app checks for new versions at start; installing a new version over the old one keeps all your data.

</details>

<div align="center"><sub>© 2026 BerkHasap</sub></div>
