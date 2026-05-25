
# 🌐 VPN / Proxy tools & configs

Мини‑канон‑лист клиентов, конвертеров подписок и конфиг‑подписок для Clash/V2Ray.

---

## 📱 Клиенты

### Desktop / CLI

- **[v2rayN (Windows)](https://github.com/2dust/v2rayN/releases)** — графический клиент для V2Ray на Windows.

- **FlClashX (Arch Linux)**  
  - `flclashx-bin` (AUR):  
    https://aur.archlinux.org/packages/flclashx-bin  
  - `flclashx-git` (AUR):  
    https://aur.archlinux.org/packages/flclashx-git  

- **Nekobox**  
  Мобильный клиент на Clash‑движке (обычно APK из GitHub‑релизов / магазинов).
# Настройка V2RayA + Xray на Arch

Инструкция по развертыванию и конфигурации легковесного и «всеядного» прокси-менеджера **v2rayA** для работы с сырыми подписками (VLESS, Shadowsocks) с GitHub без использования сторонних конвертеров. Отлично работает в Wayland-окружении.

## 🔗 Полезные ссылки

* **Пакет в AUR:** [v2raya-bin](https://aur.archlinux.org/packages/v2raya-bin) *(используется pre-compiled версия для экономии ресурсов и времени установки)*
* **Официальный репозиторий:** [v2rayA / v2rayA](https://github.com/v2rayA/v2rayA)
* **Локальная веб-панель:** [http://localhost:2017/](http://localhost:2017/)

---

## 💻 Управление службами (CLI)

Для экономии оперативной памяти и ресурсов процессора автозапуск отключен. Службы запускаются вручную по необходимости.

**Запуск прокси и веб-интерфейса:**
```bash
sudo systemctl start v2raya xray
```

**Полная остановка и выгрузка из системы:**
```bash
sudo systemctl stop v2raya xray
```

*Примечание: При ручном запуске бинарника без root-прав используйте флаг:* `v2raya --lite`

---

## 🛠️ Рабочий конфиг v2rayA

Стабильные настройки, проверенные на совместимость с сетевым стеком CachyOS:


| Параметр | Значение | Описание |
| :--- | :--- | :--- |
| **Прозрачный прокси / Системный прокси** | `Включено: Режим разделения трафика такси` | Глобальный перехват трафика системы |
| **Реализация прозрачного прокси** | `redirect` | Перенаправление пакетов через iptables |
| **Режим разделения трафика на порте** | `RoutingA` | Маршрутизация по встроенным правилам |
| **Предотвратить DNS-спуфинг** | `Перенаправлять DNS запросы` | Защита от утечки реального DNS провайдера |
| **Специальный режим** | `Выключено` | Стандартный режим работы |
| **TCPFastOpen** | `По-умолчанию` | Оптимизация TCP-соединений |
| **Сниффер** | `Http + TLS + Quic` | Анализ пакетов (включая QUIC-трафик YouTube) |
| **Мультиплекс** | `Выключено` | Стабильное разделение потоков данных |

### 💡 Эксперименты с производительностью
Если необходимо поэкспериментировать со скоростью загрузки или исправить конфликты сетевого экрана, можно попробовать повключать/выключать тумблер **IP форвардинг** (`IP Forwarding`) в правом верхнем углу интерфейса.

---

## 📸 Скриншот конфигурации

<img width="636" height="523" alt="v2rayA Working Configuration" src="https://github.com/user-attachments/assets/5b0e170a-b23a-438e-8a5b-ba99de034557" />
 

---

## 🔗 Подписки и конвертеры

### Конвертеры Clash‑подписок

- **Sub‑конвертер (подписки → Clash)**  
  https://sub.com.mp/

- **Пример использования конвертера**  
  https://arx.cc/  
  Например:  
  https://arx.cc/https://raw.githubusercontent.com/igareck/vpn-configs-for-russia/refs/heads/main/Vless-Reality-White-Lists-Rus-Mobile.txt

---

## 📂 Конфиг‑подписки

### Whitelist / GFW‑bypass

- **Whitelist‑конфиги для России**  
  https://github.com/jsxta/whitelist-russia

- **Простые конфиги (GFW‑bypass и т.п.)**  
  https://gbr.mydan.online/configs

- **Комплексные конфиги для России**  
  https://github.com/igareck/vpn-configs-for-russia
  https://github.com/zieng2/wl
  
https://cdn.jsdelivr.net/gh/igareck/vpn-configs-for-russia@main/Vless-Reality-White-Lists-Rus-Mobile.txt

https://cdn.statically.io/gh/igareck/vpn-configs-for-russia@main/Vless-Reality-White-Lists-Rus-Mobile.txt

https://rawcdn.githack.com/igareck/vpn-configs-for-russia/main/Vless-Reality-White-Lists-Rus-Mobile.txt

https://raw.githack.com/igareck/vpn-configs-for-russia/main/Vless-Reality-White-Lists-Rus-Mobile.txt

https://cdn.jsdelivr.net/gh/igareck/vpn-configs-for-russia@main/Vless-Reality-White-Lists-Rus-Mobile-2.txt

https://cdn.statically.io/gh/igareck/vpn-configs-for-russia@main/Vless-Reality-White-Lists-Rus-Mobile-2.txt

https://rawcdn.githack.com/igareck/vpn-configs-for-russia/main/Vless-Reality-White-Lists-Rus-Mobile-2.txt

https://raw.githack.com/igareck/vpn-configs-for-russia/main/Vless-Reality-White-Lists-Rus-Mobile-2.txt

https://cdn.jsdelivr.net/gh/igareck/vpn-configs-for-russia@main/WHITE-CIDR-RU-all.txt

https://cdn.statically.io/gh/igareck/vpn-configs-for-russia@main/WHITE-CIDR-RU-all.txt

https://rawcdn.githack.com/igareck/vpn-configs-for-russia/main/WHITE-CIDR-RU-all.txt

https://raw.githack.com/igareck/vpn-configs-for-russia/main/WHITE-CIDR-RU-all.txt



- **Дополнительные whitelist‑подборки**  
  https://github.com/zieng2/wl

- **Конфиги/подписки от `rjsxrd`**  
  https://github.com/whoahaow/rjsxrd

---

### Проекты‑подписки

- **EtoNeYaProject**  
  - Вариант 1:  
    https://raw.githubusercontent.com/EtoNeYaProject/etoneyaproject.github.io/refs/heads/main/1  
  - Вариант 2:  
    https://raw.githubusercontent.com/EtoNeYaProject/etoneyaproject.github.io/refs/heads/main/2  
  - Через CDN:  
    https://cdn.jsdelivr.net/gh/EtoNeYaProject/EtoNeYaProject.github.io@refs/heads/main/1  
  - Зеркало:  
    https://etoneya.a9fm.site/2

- **Alley.serv00**  
  https://alley.serv00.net/1  
  https://alley.serv00.net/2

---

## 🧰 Генераторы конфигураций

### V2Ray / Clash‑конфиг‑генератор

- **[ConfigForge‑V2Ray](https://shatakvpn.github.io/ConfigForge-V2Ray/)** — генератор конфигов V2Ray/Clash.

---

## ⚠️ Не проверенные / заметки

- **Whitelist‑VPN‑правила (4pda‑стиль)** — *не проверено*  
  https://raw.githubusercontent.com/bywarm/whitelists-vpns-etc/refs/heads/main/whitelists1-4pda.txt


==app==
https://github.com/2dust/v2rayN/releases
nekobox +-
flclashx
https://aur.archlinux.org/packages/flclashx-bin
https://aur.archlinux.org/packages/flclashx-git
==
sub converter subscribe clash
https://sub.com.mp/
example
https://arx.cc/
https://arx.cc/https://raw.githubusercontent.com/igareck/vpn-configs-for-russia/refs/heads/main/Vless-Reality-White-Lists-Rus-Mobile.txt
==
==conf==

https://github.com/jsxta/whitelist-russia
https://gbr.mydan.online/configs
https://github.com/igareck/vpn-configs-for-russia
https://github.com/zieng2/wl
https://github.com/whoahaow/rjsxrd
https://raw.githubusercontent.com/EtoNeYaProject/etoneyaproject.github.io/refs/heads/main/1
https://raw.githubusercontent.com/EtoNeYaProject/etoneyaproject.github.io/refs/heads/main/2
https://cdn.jsdelivr.net/gh/EtoNeYaProject/EtoNeYaProject.github.io@refs/heads/main/1
https://etoneya.a9fm.site/2
https://alley.serv00.net/1
https://alley.serv00.net/2
 Генератор конфигов:
https://shatakvpn.github.io/ConfigForge-V2Ray/

- **V2RayA + xray**
- https://aur.archlinux.org/packages/v2raya-bin
- https://github.com/v2rayA/v2rayA
- v2raya --lite
- http://localhost:2017/
- sudo systemctl start v2raya xray
- sudo systemctl stop v2raya xray
- [v2rayA + Xray: Рабочий конфиг]

1. Прозрачный прокси/Системный прокси: Включено: Режим разделения трафика такси (System Proxy / Перехват трафика)
2. Реализация прозрачного прокси: redirect (Перенаправление через iptables)
3. Режим разделения трафика на порте с правилами: RoutingA (Маршрутизация по встроенным правилам)
4. Предотвратить DNS-спуфинг: Перенаправлять DNS запросы (Защита от утечки DNS)
5. Специальный режим: Выключено
6. TCPFastOpen: По-умолчанию
7. Сниффер: Http + TLS + Quic (Анализ всех типов веб-пакетов, включая YouTube)
8. Мультиплекс: Выключено

<img width="636" height="523" alt="image" src="https://github.com/user-attachments/assets/5b0e170a-b23a-438e-8a5b-ba99de034557" />
можно ip forward ... попробовать повключать повыключать



not checked:
https://raw.githubusercontent.com/bywarm/whitelists-vpns-etc/refs/heads/main/whitelists1-4pda.txt
