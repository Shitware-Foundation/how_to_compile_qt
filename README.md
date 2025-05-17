# Как компилировать славянский Qt?
1. Создание файлов
   - Создайте .pro файл
   ```
   TEMPLATE = app
   TARGET = slavicqt
   QT += widgets
   SOURCES += app.spp_temp.cpp
   ```
   - Создайте app.spp файл (программу)
   ```
   #подключати <QApplication>
   #подключати <QPushButton>
   цифра царь_батюшка_главный(число argc, буква *argv[]) {
       QApplication app(argc, argv);
       QPushButton button("Славься Русь!");
       button.show();
       возвращати app.exec();
   }
   ```
2. Компиляция
   - Установите в SlavicCompiler компилятор C++, например, G++ (инструкция в репозитории славянского C)
   - Скомпилируйте .spp-файл (не обращайте внимание на ошибки!!!)
   - Запустите команды: `qmake && make`
4. Запуск
   - Для запуска введите команду: `./slavicqt`
