---
layout: default
permalink: hardware
---
## Какую ноду выбрать для покупки или сборки?

### Что есть в природе

Полный список поддерживаемых устройств (Officially Supported и Community Supported) можно посмотреть в [официальном прошивальщике](https://flasher.meshtastic.org/) при выборе оборудования.


Популярные устройства от [Heltec](https://heltec.org/product-category/lora/meshtastic/), на [AliExpress](https://aliexpress.ru/wholesale?SearchText=heltec+meshtastic)

Готовое портативное устройство [T-Echo](https://lilygo.cc/products/t-echo-meshtastic) от [LilyGo](https://lilygo.cc/collections/lilygo-with-meshtastic)

Обратите внимание! Нижегородская mesh-сеть работает на частоте **433МГц**, частота 868МГц тоже развивается, но на данный момент таких узлов мало.
Учитывайте это при покупке / заказе оборудования.

### Что проверено и рекомендуется

В сети протестированы и стабильно работают сборки на основе двух проектов:

#### Мобильная нода:

[Heltec ESP32 LoRa](https://sl.aliexpress.ru/p?key=TzWbV41) одно-платник (Heltec Wireless tracker)

#### Стационарная нода:

[MeshAdventurer](https://github.com/chrismyers2000/MeshAdventurer)

С использованием радиомодулей от Ebyte [SX1268 E22-400M33S](https://www.cdebyte.com/products/E22-400M33S) и [SX1262 E22-900M33S](https://www.cdebyte.com/products/E22-900M33S).
При заказе обратите внимание на букву `M` в маркировке радиомодуля, она означает интерфейс подключения по SPI.
Существуют так же радиомодули c буквой `T` в маркировке, это означает интерфейс подключения UART.
MeshAdventurer спроектирован для использования радиомодулей с SPI интерфейсом.

#### Аксессуары.

[Корпус для одно-платника](https://www.printables.com/model/616628-heltec-wireless-tracker-case-for-meshtastic/files)

[Аккумулятор 21700](https://ozon.ru/t/Q1ePOub)

Антенна, которая хорошо работает с портативными устройствами на частоте 433 МГц: [Retevis RHD-771, 36,5cm VHF UHF (SMA - male)](https://ozon.ru/t/NIXREqy)

Дефолтная антенна из коробки имеет крайне низкую эффективность работы для приема и ретрансляции, так как у нее резонанс около 488МГц (необходимый 434МГц). Ее использовать не стоит, есть смысл сразу же заказать более эффективную.

[Переходник радиомодуль-антенна](https://ozon.ru/t/fcd6CAb) с низким затуханием.
