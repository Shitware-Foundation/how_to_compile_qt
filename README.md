# Как компилировать славянский Qt?
1. Создание файлов
   - Создайте .pro файл
   ```
   TEMPLATE = app
   TARGET = slavicqt
   CONFIG += console
   CONFIG -= qt
   SOURCES += app.spp_temp.cpp
   ```
   - Создайте app.spp файл (программу)
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
   - Скомпилируйте .spp-файл (не обращайте внимание на ошибки!!!)
   - Запустите команды: `qmake && make`
3. Запуск
   - Для запуска введите команду: `./slavicqt`
