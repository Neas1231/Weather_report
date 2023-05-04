# ___Weather Report___
### Weather image classification model
Классификатор картинок 10 погодных условий и класса "Нет погоды"
## Описание полученных результатов
1. __Папка notebooks__ <br />
___Содержит в себе папки и файлы:___ <br />
        - __Train models__ - папка с файлами расширения ipynb с кодом обучения моделей классификации картинок погоды <br />
        В ходе заполнения папки было проведена работа по подбору гиперпараметров, предобученных моделей и остальных не мало важных конфигураций. Самая лучшая модель была подобрана по наилучшему параметру loss из всех обученных эпох и по матрице метрик, выведенной в файле Models_test.ipynb <br />
        - __EDA.ipynb__ - представление собранного из сети интернет датасета и дополненного классом "No weather" <br />
        - __Models_test.ipynb__ - выведение метрик по каждому классу обученной модели с помощью сохранённой части данных не использованных при обучении и валидации <br />
        - __Inference.ipynb__ - пример работы обученной модели по распознаванию погоды на картинке с графическим выводом
2. __Папка api__ <br />
___Представляет собой веб приложение основанное на библиотеке streamlit для развёртывания обученной модели___ <br />
___Содержит папки и файлы:___ <br />
        - __Requirements.txt__ - необходимые установленные библиотеки в среде компилятора для запуска API <br />
        - __style.css__ - настройки стиля сайта, дополнение визуала интерфейса <br />
        - __weather.py__ - основной код веб приложения развёртывания получившейся модели <br />
        - __weights-no_weather_class-efinetb4-bestloss.pth__ - веса для модели, которые были полученны при обучении и валидации множества различных предобученных классификаторов <br />
3. __Файл Readme.md__ <br />
__Сам текстовый документ содержащий полезную информацию по репозиторию и самому проекту__
## Инструкция для установки веб приложения на свой компьютер.
Для начала чтобы запустить созданную нами API нужно установить требующиеся библиотеки и открыть её с помощью консоли. <br />
Но для того чтобы консоль смогла работать с средой нужно установить python и указать его IDLE для cmd. <br />
Для начала проверьте настроен ли уже python у вас в cmd написав в командной строке 'python' <br />
Если cmd вывела версию установленного пайтона значит он настроен и вы можете пропускать следующие пункты. <br />
- Также попробуте перед установкой самой версии python указать галочку на против Add python.exe to PATH и проверить сработала ли установка в cmd всё той же командой 'python'
Если автоматический метод не сработал: <br />
1. Скачайте любую версию python <br />
2. Найдите путь к файлу pythonw.exe в файлах python, открывающуюся через ярлык IDLE. <br />
Для меня это путь: C:\Users\[Пользователь]\AppData\Local\Programs\Python\Python39 <br />
3. В настройках находим раздел Система и в нём находим вкладку Дополнительные параметры системы <br />
4. В параметрах во вкладке дополнительно открываем Переменные среды <br />
5. Ищем Системные переменные и открываем переменную Path двойным кликом <br />
6. Нажимаем кнопку Создать и создаём переменную с путём к pythonw, который мы нашли в предыдущих пунктах. <br />
7. Везде нажимаем ОК и открываем cmd <br />
8. Прописываем команду 'python' и если строка вывела версию установленного пайтона всё было проделано правильно и cmd готова к установке библиотек

### Установка библиотек
Далее открыв cmd заново впишите по очереди следующие строки для установки библиотек: <br />

py -m pip install streamlit <br />
py -m pip install pandas <br />
py -m pip install Pillow <br />
py -m pip install streamlit-on-Hover-tabs <br />
py -m pip install torch <br />
py -m pip install torchvision <br />
py -m pip install PyDrive <br />

### Установка API и модели

-Скачайте github репозиторий по ссылке: https://github.com/Neas1231/Weather_Test <br />
-Распакуйте скачанные файлы в папку с используемым пользователем <br />
 У нас это путь: C:\Users\nicka <br />

### Открытие API

После того как все файлы были скачаны и установлены в нужное место, можно открывать нашу API через cmd <br />
-Введите команду py -m streamlit run weather.py <br />
Streamlit может попросить ваш mail, но вводить его не обязательно, просто нажимаете Enter и API должна открыться в браузере установленном по умолчанию.
## Пример работы веб приложения:
![Weather report (1)](https://user-images.githubusercontent.com/120177610/236161416-a881eec7-d87e-4b24-98e0-99e18eb04d52.gif)
