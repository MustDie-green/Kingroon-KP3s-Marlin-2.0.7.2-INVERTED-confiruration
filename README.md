# Kingroon-KP3s-Marlin-2.0.7.2-INVERTED-confiruration
I have an inverted version of Kingroon KP3S, so I made an inverted configuration by modification cfg file from [dulfe's configuration](https://github.com/dulfe/Kingroon-KP3S-Marlin). (dulfe thank you so much for it)
I also changed AXIS_STEPS_PER_UNIT, beacuse 160 steps per mm made my printed mad, it needs 80 steps.

# Файл конфигурации для прошивки Marlin 2.0.7.2 для принтера Kingroon KP3s
Поскольку у меня была инвертированная версия принтера, а на просторах интернета не было ни прошивки, ни конфиг-файла для прошивки для инвертированных принтеров, я сделал свою конфигурацию. За основу взял файлы по ссылке выше, инвертировал моторы и изменил количество шагов на мм.

Принтер инвертирован с завода, если что, — с каких-то партий стали ставить новые моторы, которые крутятся в другую сторону. Чтобы принтер работал как надо, их инвертируют через конфигурацию прошивки.


# **USE IT AT YOUR OWN RISK** 
**I am not resposnsible for any problems etc** 
I'm not even a programmer, I'm psychologist;)
All notes and instructions from https://github.com/dulfe/Kingroon-KP3S-Marlin is actual for these files, you just need to use my files. 
Below is only Russian.

# **Используйте файлы конфигурации и самостоятельно собранные прошивки только на свой страх и риск**
У меня все работает, но я даже не программист, я психолог ;)

## Доп инфа
- Конфигурация под драйвера A4988, по идее должна работать с драйверами TMC2225
- После установки прошивки вам лучше сделать калибровку PID (про это и установку прошивки есть в видео https://www.youtube.com/watch?v=zCykGT77myQ)
- Если экран у вас повернут в одной ориентации, а сенсор как будто в другой, то зажмите пальцем на несколько секунд в любую пустую область, это должно включить калибровку
- Конфигурация под версию Marlin 2.0.7.2. Вы можете переделать этот конфиг под актуальную версию, я бы это сделал, но мне пока влом.

## Что делать с файлом конфигурации? (Как собрать прошивку Marlin)
Инструкция переведена и дополнена из того же репозитория по ссылке выше
- Установить [Visual Studio Code](https://code.visualstudio.com/Download)
- Установить в нем расширение [PlatformIO Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
- Установить там же расширение [Auto Build Marlin Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MarlinFirmware.auto-build).
- Скачать исходники Marlin 2.0.7.2 [с их страницы на гитхабе](https://github.com/MarlinFirmware/Marlin/releases/tag/2.0.7.2) (там надо скачать Sourсe code.zip)
- Распаковать их (Например в `c:\sources\marlin`)
- Скопировать файлы `Configuration.h` и `Configuration_avd.h` из этого репозитория в папку `Marlin` с заменой, которая находится в папке, которую вы только что создали. (Например в `c:\sources\marlin\Marlin`)
- Дальше следовать инструкции из [Auto Build Marlin](https://marlinfw.org/docs/basics/auto_build_marlin.html).

## Как установить прошивку?
- После компилляции прошивки идите в папку `<папка с исходниками прошвики>\.pio\build\mks_robin_nano35\Robin_nano35.bin`, копируйте этот файл на вашу Micro SD карту
- Переименуйте файл в robin_nano.bin
- Дальше по видео https://www.youtube.com/watch?v=zCykGT77myQ

### Если будут еще какие-то вопросы, можете писать в тг чат https://t.me/kingroonkp3_chat
Возможно, на какие-то ваши вопросы даже отвечу я, я там не админ, просто сижу.
За помощь с решением проблем с этим конфигом ОГРОМНОЕ спасибо RisaWildman из этого чата, именно она помогла мне найти проблему с лишними шагами на мм.
