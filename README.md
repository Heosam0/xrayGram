🇷🇺 Русский

В связи с жесткими блокировками и замедлением Telegram, стандартный MTProxy перестал справляться со своей задачей. Протоколы на базе XRay (например, VLESS) показывают себя гораздо устойчивее к DPI-фильтрам, а поднять или найти такой сервер сейчас зачастую проще, чем классический прокси. Поэтому этот форк добавляет нативную поддержку XRay прямо в клиент Telegram.

  ⚠️ Важное уточнение об авторстве: > Вся основа этого форка — интеграция ядра XRay-core, поддержка подписок, парсинг конфигов из буфера обмена и авто-тестинг пинга серверов — была разработана оригинальным автором форка. Мой вклад заключается в компиляции готовой сборки и добавлении полной бесшовной интеграции XRay в интерфейс Telegram.

Что реализовано:

Базовый функционал (от оригинального автора):

 - Добавление конфигураций прямо из буфера обмена.
 - Поддержка подписок (в том числе с привязкой к HWID).
 - Автоматическое тестирование серверов и проверка пинга.

Интеграция в интерфейс (добавлено в этой сборке):

 - Нативная поддержка ссылок: Ссылки форматов vless://, vmess:// и trojan:// теперь распознаются клиентом и становятся кликабельными прямо в чатах.
 - Бесшовный UI: При клике на ссылку открывается родное красивое диалоговое окно Telegram с предложением добавить прокси (без костылей и перехода в другие приложения).
 - Перехват из системы (Deep Links): Ссылки корректно открываются из браузера и других приложений, сразу перенаправляя вас в настройки прокси внутри клиента.

🇬🇧 English

Due to severe blocks and throttling of Telegram, the standard MTProxy is no longer sufficient. XRay-based protocols (like VLESS) are much more resistant to DPI filters, and finding or deploying such a server is often easier now. This fork adds native XRay support directly into the Telegram client.

   ⚠️ Important Attribution Note: > The entire core of this fork — the XRay-core integration, subscription support, clipboard config parsing, and auto-testing of servers — was developed by the original fork author. My contribution consists of compiling the ready-to-use build and adding full, seamless integration of XRay into the Telegram UI.

Features:

Core Functionality (by original author):

 - Adding configurations directly from the clipboard.
 - Subscription support (including HWID-locked subscriptions).
 - Automatic server testing and ping checks.

UI & System Integration (added in this build):

 - Native Deep Links: vless://, vmess://, and trojan:// links are now recognized by the client and are fully clickable directly inside chats.
 - Seamless UI: Clicking an XRay link opens the native, clean Telegram dialog asking to add the proxy (no workarounds or external apps needed).
 - System Interception: Links open correctly from the browser and other apps, directly launching the client's proxy settings.
