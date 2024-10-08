## C чего начать? 

## Настройка оборудования (игровой компьютер)

1. Установите вашу DMA карту в свободный слот PCIe на вашей материнской плате игрового компьютера. DMA-карты имеют PCI-e x1 и могут быть установлены в слоты x1, x4, x8, x16.

2. Подключите DMA карту через USB Type-C - USB 3.0 к cофт ПК (2-й ПК, обязательно подключите к синему разъёму USB обозначающему порт 3.0) с помощью USB-кабеля (Уточню, что требуется именно USB 3.0).

3. Настройте следующие параметры в BIOS игрового ПК:
- Нужно отключить виртуализацию на вашем компьютере, так как она может препятствовать доступу к памяти DMA. 
- Выключите все параметры cвязанные с виртуализацией в BIOS вашей системы.
  
**На материнских платах с процессорами Intel этот пункт обычно указан как:**
- Virtualization / IOMMU / VT-d
  
**На материнских платах для процессоров AMD этот параметр обычно указан как:**
- Virtualization / IOMMU / SVM Mode
  
Отключите **NX-Bit** (Только если он доступен, если вы не можете найти его, пропустите этот этап). 

При необходимости установите PCIслот DMA карты с Auto на Gen1 (Advanced > PCIe Settings).

## Настройка 2 ПК (Софт ПК)

1. Установка драйвера FTDI (Софт ПК)
   
- Вам нужно установить драйвер для Windows x64 с сайта [https://ftdichip.com/drivers/d3xx-drivers/](https://ftdichip.com/wp-content/uploads/2024/06/FTD3XXDriver_WHQLCertified_v1.3.0.10.zip)
  
- После загрузки архива распакуйте все содержимое в папку на рабочем столе.

- Зайдите в папку, щелкните правой кнопкой мыши по файлу **ftdibus3.inf** и нажмите кнопку **Установить**.
  ![alt text](https://i.imgur.com/tZwFH6a.png) 
- Убедитесь что он отображается в Диспетчере устройств > Контроллеры USB
  ![alt text](https://i.imgur.com/kAAEDdf.png)

2. Тест DMA (Софт ПК)
- Cкачайте и распакуйте [DMA Test](https://mega.nz/file/nHIiVByK#1M95TRTO2VdJHSZvwrFJt3ZpF9o-y7D1eRVJtbWidqk)
- Запустите тест lone-dma-test.exe на вашем Софт ПК и нажмите 1 (Full Test)
- Если вы настроили все правильно будет указано что тест ПРОЙДЕН.
  
Результаты Speed Test: 

- Меньше 4000 - Плохо

- 4000+ - Пойдет, играбельно

- 5000+ - Хорошо 

- 6000+ - Отлично

Результаты Throughput Test:

- Меньше 100 - Плохо 

- 100+ - Приемлемо 

- 150+ - Хорошо

- 200+ - Отлично
   


