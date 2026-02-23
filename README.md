# ⚡ EssentialsMod

![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1-green?style=for-the-badge&logo=mojangstudios)
![Forge](https://img.shields.io/badge/Forge-47+-orange?style=for-the-badge&logo=gradle)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

> 🔥 **EssentialsX** — аналог легендарного плагина, но в виде **Forge-мода** для Minecraft 1.20.1.
> Домашние точки, варпы, телепортации, экономика, модерация, почта — все базовые инструменты сервера в одном моде.

---

## 📚 Содержание
- [✨ Возможности](#-возможности-план)
- [🚀 Установка](#-установка)
- [🛠️ Сборка из исходников](#%EF%B8%8F-сборка-из-исходников)
- [🛡️ Права доступа](#%EF%B8%8F-права-доступа)
  - [Навигация и телепортация](#-навигация-и-телепортация)
  - [Экономика](#-экономика)
  - [Коммуникация и поддержка](#-коммуникация-и-поддержка)
  - [Персонализация и профиль](#-персонализация-и-профиль)
  - [Игровые утилиты и комфорт](#-игровые-утилиты-и-комфорт)
  - [Инвентарь и предметы](#-инвентарь-и-предметы)
  - [Модерация и безопасность](#-модерация-и-безопасность)
  - [Администрирование мира и сервера](#-администрирование-мира-и-сервера)
  - [Префиксные права](#-префиксные-права)

---

## ✨ Возможности (план)

- 🏠 **Дома** — `/sethome`, `/home` — **готово**
- 🌀 **Варпы** — `/setwarp`, `/warp` — **готово**
- ⭐ **Точка спавна** — `/spawn`, `/setspawn` — **готово**
- 👥 **Телепортации** — `/tpa`, `/tpahere`, `/tpaccept` — **готово**
- 📦 **Киты** — стартовые наборы с кулдауном — **готово**
- 💰 **Экономика** — внутренняя валюта, баланс игроков — **готово**
- 🔨 **Модерация** — `/kick`, `/ban`, `/mute`, `/jail` — **готово**
- 📨 **Сообщения** — приватный чат и внутренняя почта — **готово**
- 🎨 **Ники и чат** — форматирование чата, цветные ники — **готово**
- 🔧 **Админ-инструменты** — `/god`, `/vanish`, `/freeze` — **готово**

---

## 🛡️ Права доступа

Все права доступа мод выдаёт в формате `essentialsx.*`. Ниже собраны все узлы из [enum `Permissions`](src/main/java/ru/ap4uuk/essentialsx/data/Permissions.java) и сгруппированы по назначению.

> ℹ️ Если вы используете LuckPerms или другой менеджер прав, просто добавьте соответствующий узел нужной группе игроков.

### 🧭 Навигация и телепортация

| Узел | Что даёт |
| --- | --- |
| `essentialsx.back` | Возврат на последнюю точку смерти или телепортации командой `/back`. |
| `essentialsx.home` | Использование базы команды `/home` для перехода домой. |
| `essentialsx.home.set` | Создание домашних точек командой `/home set <имя>`. |
| `essentialsx.home.delete` | Удаление сохранённых домов через `/home delete`. |
| `essentialsx.home.use` | Телепортация к любому своему дому. |
| `essentialsx.home.unlimited` | Снятие ограничений на количество домов. |
| `essentialsx.delhome` | Быстрое удаление дома командой `/delhome`. |
| `essentialsx.sethome` | Альтернативная команда `/sethome` для установки дома. |
| `essentialsx.tp` | Мгновенная телепортация к игроку через `/tp`. |
| `essentialsx.tpaccept` | Подтверждение входящих запросов на телепорт `/tpaccept`. |
| `essentialsx.tpdeny` | Отклонение запросов `/tpdeny`. |
| `essentialsx.tpa` | Доступ к команде `/tpa` (отправка запросов на телепортацию). |
| `essentialsx.tpa.send` | Возможность отправлять запросы `/tpa` при тонкой настройке групп. |
| `essentialsx.tpa.accept` | Принятие запросов `/tpa`. |
| `essentialsx.tpa.deny` | Отклонение запросов `/tpa`. |
| `essentialsx.tphere` | Телепортация игрока к себе (`/tpahere`). |
| `essentialsx.tppos` | Перемещение к указанным координатам (`/tppos`). |
| `essentialsx.admin.spawn` | Телепортация себя или выбранного игрока на общий спавн (`/spawn`). |
| `essentialsx.admin.spawn.set` | Установка точки спавна сервера (`/setspawn`). |
| `essentialsx.setwarp` | Создание нового варпа командой `/setwarp` (наследный алиас). |
| `essentialsx.warp` | Использование команды `/warp` и просмотр списка варпов. |
| `essentialsx.warp.set` | Создание варпов через `/warp set`. |
| `essentialsx.warp.delete` | Удаление варпов (`/warp delete`). |
| `essentialsx.warp.list` | Просмотр списка варпов даже при ограничениях. |
| `essentialsx.warp.use` | Телепортация к варпам. |
| `essentialsx.warp.unlimited` | Снятие лимитов на количество создаваемых варпов. |

### 💰 Экономика

| Узел | Что даёт |
| --- | --- |
| `essentialsx.balance` | Просмотр собственного баланса (`/balance`). |
| `essentialsx.balance.others` | Проверка баланса других игроков. |
| `essentialsx.eco` | Администрирование экономики (`/eco`, выдача и изъятие валюты). |
| `essentialsx.pay` | Переводы между игроками (`/pay`). |

### 💬 Коммуникация и поддержка

| Узел | Что даёт |
| --- | --- |
| `essentialsx.chat.color` | Использование цветовых кодов в чат-сообщениях. |
| `essentialsx.chat.format` | Продвинутое форматирование чата (жирный, курсив и т.д.). |
| `essentialsx.helpop` | Отправка запросов модераторам через `/helpop`. |
| `essentialsx.helpop.receive` | Получение сообщений `/helpop` от игроков. |
| `essentialsx.helpop.reply` | Ответы на обращения `/helpop`. |
| `essentialsx.mail` | Доступ к личной почте (`/mail`). |
| `essentialsx.mail.send` | Отправка писем другим игрокам. |
| `essentialsx.mail.sendall` | Массовая рассылка писем всем игрокам. |
| `essentialsx.admin.clearchat` | Очистка глобального чата командой `/clearchat`. |
| `essentialsx.admin.broadcast` | Глобальные объявления через `/broadcast`. |
| `essentialsx.list` | Просмотр списка игроков онлайн (`/list`). |
| `essentialsx.list.hidden` | Видимость скрытых/невидимых игроков в `/list`. |
| `essentialsx.help` | Просмотр внутриигровой справки `/help`. |
| `essentialsx.motd` | Просмотр сообщения дня при входе и командой `/motd`. |
| `essentialsx.rules` | Ознакомление с правилами сервера через `/rules`. |

### 🧑 Персонализация и профиль

| Узел | Что даёт |
| --- | --- |
| `essentialsx.nick` | Изменение собственного никнейма (`/nick`). |
| `essentialsx.nick.color` | Цветовые коды в нике. |
| `essentialsx.nick.format` | Форматирование ника (стили текста). |
| `essentialsx.nick.reset.others` | Сброс чужих никнеймов до оригинала. |
| `essentialsx.realname` | Просмотр реального ника игрока, даже если установлен псевдоним. |
| `essentialsx.playtime` | Просмотр собственного игрового времени. |
| `essentialsx.playtime.others` | Проверка времени других игроков. |
| `essentialsx.admin.whois` | Расширенная информация о игроке (`/whois`). |

### 🛠️ Игровые утилиты и комфорт

| Узел | Что даёт |
| --- | --- |
| `essentialsx.afk` | Ручной перевод в режим «AFK». |
| `essentialsx.afk.exempt` | Иммунитет к авто-кику или уведомлениям за AFK. |
| `essentialsx.feed` | Восполнение сытости командой `/feed`. |
| `essentialsx.feed.others` | Кормление других игроков. |
| `essentialsx.fly` | Включение режима полёта. |
| `essentialsx.god` | Режим бессмертия для себя. |
| `essentialsx.god.others` | Включение/отключение бессмертия другим игрокам. |
| `essentialsx.heal` | Исцеление себя. |
| `essentialsx.heal.others` | Исцеление других игроков. |
| `essentialsx.effect` | Наложение эффектов на себя командой `/effect`. |
| `essentialsx.effect.others` | Управление эффектами других игроков. |
| `essentialsx.hat` | Надеть предмет из руки как шляпу (`/hat`). |
| `essentialsx.suicide` | Совершить самоубийство командой `/suicide`. |

### 🎒 Инвентарь и предметы

| Узел | Что даёт |
| --- | --- |
| `essentialsx.admin.clearinventory` | Очистка собственного инвентаря. |
| `essentialsx.admin.clearinventory.others` | Очистка инвентаря других игроков. |
| `essentialsx.enderchest.small` | Базовый размер эндер-сундука. |
| `essentialsx.enderchest.large` | Расширенный эндер-сундук. |
| `essentialsx.enderchest.other` | Просмотр эндер-сундуков других игроков. |
| `essentialsx.kit` | Получение наборов `/kit`. |
| `essentialsx.kit.create` | Создание новых китов. |
| `essentialsx.kit.delete` | Удаление наборов. |
| `essentialsx.repair` | Починка предмета в руке. |
| `essentialsx.repair.all` | Починка всех предметов. |
| `essentialsx.repair.armor` | Починка только брони. |

### 🛡️ Модерация и безопасность

| Узел | Что даёт |
| --- | --- |
| `essentialsx.admin.ban` | Перманентные баны игроков. |
| `essentialsx.admin.tempban` | Временные блокировки `/tempban`. |
| `essentialsx.ban.exempt` | Иммунитет к бану. |
| `essentialsx.tempban.exempt` | Иммунитет к временным банам. |
| `essentialsx.ban.notify` | Уведомления о банах. |
| `essentialsx.ban.force` | Принудительное применение бана, игнорируя иммунитет. |
| `essentialsx.tempban.notify` | Уведомления о временных блокировках. |
| `essentialsx.tempban.force` | Принудительные временные баны. |
| `essentialsx.admin.mute` | Перманентные муты (`/mute`). |
| `essentialsx.admin.tempmute` | Временные муты (`/tempmute`). |
| `essentialsx.mute.exempt` | Иммунитет к муту. |
| `essentialsx.mute.notify` | Уведомления о муте. |
| `essentialsx.mute.force` | Принудительные муты поверх иммунитета. |
| `essentialsx.tempmute.notify` | Оповещения о временных мутах. |
| `essentialsx.tempmute.force` | Принудительные временные муты. |
| `essentialsx.admin.jail` | Посадить игрока в тюрьму (`/jail`). |
| `essentialsx.admin.setjail` | Настройка точек тюрьмы. |
| `essentialsx.jail.exempt` | Иммунитет к заключению. |
| `essentialsx.jail.notify` | Уведомления о посадке в тюрьму. |
| `essentialsx.admin.kick` | Кик игроков (`/kick`). |
| `essentialsx.kick.exempt` | Иммунитет к кикам. |
| `essentialsx.kick.notify` | Уведомления о киках. |
| `essentialsx.admin.kill` | Команда `/kill` против других игроков. |
| `essentialsx.kill.exempt` | Иммунитет к принудительному убийству. |
| `essentialsx.kill.force` | Игнорирование иммунитета при `/kill`. |
| `essentialsx.admin.invsee` | Просмотр инвентаря игрока (`/invsee`). |
| `essentialsx.admin.spy` | Перехват личных сообщений (social spy). |
| `essentialsx.admin.vanish` | Невидимость для других игроков. |
| `essentialsx.vanish.see` | Возможность видеть невидимых игроков. |

### 🌍 Администрирование мира и сервера

| Узел | Что даёт |
| --- | --- |
| `essentialsx.admin.gc` | Просмотр состояния памяти и GC-сборка (`/gc`). |
| `essentialsx.gamemode` | Смена собственного режима игры. |
| `essentialsx.gamemode.others` | Смена режима другим игрокам. |
| `essentialsx.admin.spawnmob` | Спавн мобов командой `/spawnmob`. |
| `essentialsx.admin.weather` | Управление погодой (`/weather`). |
| `essentialsx.admin.time` | Настройка времени суток (`/time`). |

### 🧩 Префиксные права

| Префикс | Как работает |
| --- | --- |
| `essentialsx.home.<число>` | Ограничение количества домов. Выдайте, например, `essentialsx.home.5`, чтобы разрешить 5 домов. |
| `essentialsx.warp.<число>` | Лимит по числу варпов, создаваемых игроком. |

