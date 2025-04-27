# Как комаилировать славянский Qt?
1. Создание файлов
   1. Создвйте .pro файл
   ```
   TEMPLATE = app
   TARGET = slavicqt
   CONFIG += console
   CONFIG -= qt
   SOURCES += app.spp_temp.cpp
   ```
   2. Создайте app.spp файл (программу)
   ```
   #подключати <QApplication>
   #подключати <QPushButton>
   цифра царь_батюшка_главный() {
       QApplication app();
       QPushButton button("Славься Русь!")
       button.show()
       возвращати app.exec()
   }
   ```
2. Компиляция
   1. Скомпилируйте .spp-файл (не обращайте внимание на ошибки!!!)
   2. Запустите команды: `qmake && make`
3. Запуск
   1. Для запуска введите команду: `./slavicqt`
