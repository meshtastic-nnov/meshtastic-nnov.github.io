---
layout: default
---
## Какую ноду выбрать для покупки или сборки?

### Что есть в природе

Полный список поддерживаемых устройств (Officially Supported и Community Supported) можно посмотреть в [официальном прошивальщике](https://flasher.meshtastic.org/) при выборе оборудования.

Обратите внимание! Нижегородская mesh-сеть работает на частоте **433МГц**, частота 868МГц тоже развивается, но на данный момент таких узлов мало.
Учитывайте это при покупке / заказе оборудования.

### Что проверено и рекомендуется

В сети протестированы и стабильно работают сборки на основе двух проектов:
#### Устройства от [Heltec](https://heltec.org/product-category/lora/meshtastic/) на [AliExpress](https://aliexpress.ru/wholesale?SearchText=heltec+meshtastic)

* [Heltec V3](https://heltec.org/project/wifi-lora-32-v3/) на [AliExpress](https://aliexpress.ru/wholesale?SearchText=heltec+lora+v3)
* [Heltec V4](https://heltec.org/project/wifi-lora-32-v4/) на [AliExpress](https://aliexpress.ru/wholesale?SearchText=heltec+lora+v4)
* [Heltec MeshPocket powerbank](https://heltec.org/project/meshpocket/) на [AliExpress](https://aliexpress.ru/wholesale?SearchText=heltec+meshpocket+power+bank) и на [Ozon](https://www.ozon.ru/category/elektronika-15500/?category_was_predicted=true&deny_category_prediction=true&from_global=true&text=meshpocket).

#### Устройства от [LilyGo](https://lilygo.cc/collections/lilygo-with-meshtastic) на [AliExpress](https://aliexpress.ru/store/2090076)

* [T-Beam](https://ali.click/5gulqb)
* [T-Echo](https://lilygo.cc/products/t-echo-meshtastic)

#### Модульные устройства от [RAKwireless](https://www.rakwireless.com/en-us/products/wisblock)

На AliExpress представлены представлены буквально одним магазином с дорогой доставкой, но которую можно размазать,
если заказывать несколько позиций(разные модули, например, температура-давление) из этого магазина.

* [StarterKit](https://ali.click/kdvlqo). Данный кит в большинстве случаев используется для сборки нод с солнечными батареями. А так же хорош в качестве DIY носимых нод из-за низкого энергопотребления.

**ВНИМАНИЕ**: у даннах модулей НЕТ защиты от переполюсовки, а JST на эту тему не стандартизирован. Всегда проверяйте полюсовку на плате, аккуме и солнечной панели ИГНОРИРУЯ цветовую маркировку проводочков.

#### Open Source решениe [MeshAdventurer](https://github.com/chrismyers2000/MeshAdventurer)

Используются продвинутые радиомодули от Ebyte [SX1268 E22-400M33S](https://www.cdebyte.com/products/E22-400M33S) и [SX1262 E22-900M33S](https://www.cdebyte.com/products/E22-900M33S).
При заказе обратите внимание на букву `M` в маркировке радиомодуля, она означает интерфейс подключения по SPI.
Существуют так же радиомодули c буквой `T` в маркировке, это означает интерфейс подключения UART.
MeshAdventurer спроектирован для использования радиомодулей с SPI интерфейсом.

#### Аксессуары

* [Солнечная панель](https://ali.click/5xnhuk) для сборки автономной ноды. Существуют так же и готовые ноды: в эту же панельку уже установлен модуль RAK и аккумуляторы. Так же замечены на Ozon, но стоимость таких нод заметно выше, чем собирать самому. В случае использования RAK можно убрать родной модуль контроля заряда и подключив его напрямую. Даже JST разъём от панели подходит, НО предварительно нужно проверить сколько выдаёт панель, т.к. сущестуют ограничения на максимальное напрямжение, 6 вольт у RAK, например. Это обычно написано в даташитах. Собирать на устройствах на базе ESP32 смысла не имеет, т.к. они много кушают и в наших широтах такие сборки не успевают заряжаться.

* [Корпус для одно-платника](https://www.printables.com/model/616628-heltec-wireless-tracker-case-for-meshtastic/files)

* [Аккумулятор 21700](https://ozon.ru/t/Q1ePOub)

* Антенна, которая хорошо работает с портативными устройствами на частоте 433 МГц: [Retevis RHD-771, 36,5cm VHF UHF (SMA - male)](https://ozon.ru/t/NIXREqy). Дефолтная антенна из коробки имеет крайне низкую эффективность работы для приема и ретрансляции, так как у нее резонанс около 488МГц (необходимый 434МГц). Ее использовать не стоит, есть смысл сразу же заказать более эффективную.

* [Переходник радиомодуль-антенна](https://ozon.ru/t/fcd6CAb) с низким затуханием.

#### Подключаемые Датчики / Телеметрия

Датчики телеметрии подключаются по шине I2C. Прежде чем покупать, убедитесь, что ваша нода её поддерживает. Нужны пины SCL и SDA
Точно поддерживает [Heltec V3](https://meshtastic.org/docs/hardware/devices/heltec-automation/lora32/?heltec=v3#meshtastic-i2c-definitions), [Heltec Wireless Stick Lite](https://meshtastic.org/docs/hardware/devices/heltec-automation/lora32/?heltec=tracker-v1.1#meshtastic-i2c-definitions-2) и [Heltec Wireless Tracker v1.1/1.2](https://meshtastic.org/docs/hardware/devices/heltec-automation/lora32/?heltec=tracker-v1.1) (листаем до раздела 

##### Температура/Давление
* BMP180 [AliExpress](https://aliexpress.ru/item/1005008419970127.html?sku_id=12000044984568779) самый простой датчик для измерения температуры воздуха и атмосферного давления
##### Температура/Давление/Влажность
* BME280 [AliExpress](https://aliexpress.ru/item/1005008100133578.html?sku_id=12000043742881909) измеряет то же самое + влажность

##### Радиация
* RadSens, большая версия [Ozon](https://www.ozon.ru/product/universalnaya-plata-modul-dozimetra-schetchika-geygera-i2c-s-derzhatelem-pod-1573406445/) плата, в которую должна вставляться большая трубка СБМ-20 (ищется на Авито, главное не перепутать с СБМ-20-1)
* RadSens, маленькая версия [Ozon](https://www.ozon.ru/product/universalnaya-plata-modul-dozimetra-schetchika-geygera-i2c-energoeffektivnaya-radsens-board-1623839352/) плата, в которую должна вставляться укороченная трубка СБМ-20-1 (также, ищется на Авито)
* Источник радиации [Ozon](https://www.ozon.ru/product/detektor-istochnika-sistemy-bezopasnosti-pozharnoy-signalizatsii-ofisnoy-kamery-metalla-1830276045/) для проверки работы дозиметра

 
