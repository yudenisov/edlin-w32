Компиляция и инсталляция пакета в Windows 10
============================================

1.  Установите Microsoft Visual Studio 2017.
2.  Запустите Visual Studio Installer.
3.  Установите пакеты по умолчанию, плюс дополнительно «Visual C++ для
    классических приложений», «C++/CLI», «Windows SDK 10.0.14393.0».
4.  Скачайте этот дистрибутив и распакуйте в одну из папок.
5.  Откройте командную строку, загрузите переменные окружения для Visual
    Studio (файл vsvarall.bat) и перейдите в эту папку.
6.  Выполните команду:

    `Nmake /f Makefile.vscpp`

7.  Дождитесь окончания компиляции и компоновки.
8.  Скопируйте готовый файл `edlinw32.exe` в нужный каталог.

Compiling and installing the package in Windows 10
==================================================

1.  Install Microsoft Visual Studio 2017
2.  Run Visual Studio Installer.
3.  Install packages by default, plus additionally ‘Visual C ++ for
    classic applications’, ‘C ++ / CLI’, ‘Windows SDK 10.0.14393.0’.
4.  Download this distribution package and unpack it into one of the
    folders.
5.  Open a command prompt, load the Visual Studio environment variables
    (the vsvarall.bat file), and go to that folder.
6.  Execute The command:

    `Nmake /f Makefile.vscpp`

7.  Wait until the compilation and linking are complete.
8.  Copy the finished `edlinw32.exe` file to the desired directory.
