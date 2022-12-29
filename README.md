# everything-recognition

Упражнение на чтение кода. Распознавание образов


Программа предназначена для распознавания различных объектов, используя веб-камеру, с помощью ```OpenCV``` — open source библиотеки компьютерного зрения, которая предназначена для анализа, классификации и обработки изображений.

Для запуска программы необходимо написать в консоли команду : ```python run.py```

Для завершения программы достаточно нажать "q".

Изначально программа настроена на распознование человеческого лица в анфас, лица в профиль и глаз. 

В качестве классификаторов используются обученные модели с помощью метода каскада Хаара и алгоритма Local Binary Patterns (LBP).

Каскада Хаара — способ обнаружения объектов на изображении, основанный на машинном обучении. Обученный каскад Хаара, принимая на вход изображение, определяет, есть ли на нем искомый объект, т.е. выполняет задачу классификации, разделяя входные данные на два класса (есть искомый объект, нет искомого объекта)

Алгоритм Local Binary Patterns — мы разбиваем изображение на части и в каждой такой части каждый пиксель сравнивается с соседними 8 пикселями

Все обученные классификаторы находятся в папке ```haarcascades```


## haarcascades

Данная папка содержит следующие обученные классификаторы, которые пользователь может использовать для классификации объектов:

* Глаза:
  * ```haarcascade_eye.xml``` (```everything-recognition/haarcascades/faces/haarcascade_eye.xml```);
* Глаза в очках:
  * ```haarcascade_eye_tree_eyeglasses.xml``` (```everything-recognition/haarcascades/faces/haarcascade_eye_tree_eyeglasses.xml```);
* Две комбинации классификаторов для определения лица кота:
  * ```haarcascade_eye_tree_eyeglasses.xml``` (```everything-recognition/haarcascades/faces/haarcascade_eye_tree_eyeglasses.xml```);
  * ```haarcascade_frontalcatface_extended.xml``` (```everything-recognition/haarcascades/faces/haarcascade_frontalcatface_extended.xml```);
* Четыре комбинации классификаторов для определения лица в анфас:
  * ```haarcascade_frontalface_alt.xml``` (```everything-recognition/haarcascades/faces/haarcascade_frontalface_alt.xml```);
  * ```haarcascade_frontalface_alt_tree.xml``` (```everything-recognition/haarcascades/faces/haarcascade_frontalface_alt_tree.xml```);
  * ```haarcascade_frontalface_alt2.xml``` (```everything-recognition/haarcascades/faces/haarcascade_frontalface_alt2.xml```);
  * ```haarcascade_frontalface_default.xml``` (```everything-recognition/haarcascades/faces/haarcascade_frontalface_default.xml```);
* Человеческое тело в полный рост:
  * ```haarcascade_fullbody.xml``` (```everything-recognition/haarcascades/faces/haarcascade_fullbody.xml```);
* Левый глаз:
  * ```haarcascade_lefteye_2splits.xml``` (```everything-recognition/haarcascades/faces/haarcascade_lefteye_2splits.xml```);
* Номерные знаки российского образца:
  * ```haarcascade_licence_plate_rus_16stages.xml``` (```everything-recognition/haarcascades/faces/haarcascade_licence_plate_rus_16stages.xml```);
* Нижняя часть тела:
  * ```haarcascade_lowerbody.xml``` (```everything-recognition/haarcascades/faces/haarcascade_lowerbody.xml```);
* Профиль лица:
  * ```haarcascade_profileface.xml``` (```everything-recognition/haarcascades/faces/haarcascade_profileface.xml```);
* Правый глаз: 
  * ```haarcascade_righteye_2splits.xml``` (```everything-recognition/haarcascades/faces/haarcascade_righteye_2splits.xml```);
* Номерные знаки российского образца:
  * ```haarcascade_russian_plate_number.xml``` (```everything-recognition/haarcascades/faces/haarcascade_russian_plate_number.xml```);
* Улыбка: 
  * ```haarcascade_smile.xml``` (```everything-recognition/haarcascades/faces/haarcascade_smile.xml```);
* Верхняя часть тела:
  * ```haarcascade_upperbody.xml``` (```everything-recognition/haarcascades/faces/haarcascade_upperbody.xml```);
* Машины: 
  * ```cars.xml``` (```everything-recognition/haarcascades/cars.xml```);
* Бананы:
  * ```banana_classifier.xml``` (```everything-recognition/haarcascades/banana_classifier.xml```);
* Шесть классификаторов для определения дорожных знаков "Ограничение максимальной скорости":
  * Четыре классификатора методом каскада Хаара на разных этапов обучения:
    * ```Speedlimit_HAAR_ 13Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/HAAR/Speedlimit_HAAR_ 13Stages.xml```);
    * ```Speedlimit_HAAR_ 15Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/HAAR/Speedlimit_HAAR_ 15Stages.xml```);
    * ```Speedlimit_HAAR_ 16Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/HAAR/Speedlimit_HAAR_ 16Stages.xml```);
    * ```Speedlimit_HAAR_ 17Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/HAAR/Speedlimit_HAAR_ 17Stages.xml```);
  * Два классификатора на основе алгоритма Local Binary Patterns:
    * ```Speedlimit_24_15Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/LBP_Size_20/Speedlimit_24_15Stages.xml```);
    * ```Speedlimit_24_15Stages.xml``` (```everything-recognition/haarcascades/road-signs/Speed Limit Signs/LBP_Size_24/Speedlimit_24_15Stages.xml```);
* Дорожный знак "Стоп":
  * ```Stopsign_HAAR_19Stages.xml``` (```everything-recognition/haarcascades/road-signs/Stop Signs/StopSign_HAAR/Stopsign_HAAR_19Stages.xml```);
* Светофор:
  * ```TrafficLight_HAAR_16Stages.xml``` (```everything-recognition/haarcascades/road-signs/Traffic Lights/HAAR/TrafficLight_HAAR_16Stages.xml```);
* Дорожный знак "Уступи дорогу":
  * ```yieldsign12Stages.xml``` (```everything-recognition/haarcascades/road-signs/Yield Signs/Yield Sign LBP/yieldsign12Stages.xml```).


## config.py

Данный файл является файлом конфигурации для программы распознования объектов. 

Фактически файл хранит в себе словарь словарей, в котором определяются следующие характеристики :

* Имя определяемого объекта
  * Путь до классификатора в формате .xml;
  * Цвет рамки в цветовом пространстве RGB при обнаружении данного объекта;
  * Отрисовка рамки. Данный параметр принимает состояние ```True``` или ```False```.

Если пользователь захочет добавить какой либо из объектов для классификации, ему будет необходимо внести изменения в данный файл с соответствующими параметрами. 

Так, например, для классификации только глаз и бананов, файл будем выглядеть следующим образом: 

```
CASCADES = {
    "Eyes": {
        "path": "haarcascades/faces/haarcascade_eye.xml",
        "color": (0, 255, 0),
        "draw": True
    },
    "cars": {
        "path": "haarcascades/cars.xml",
        "color": (255, 255, 255),
        "draw": True
    }
}
```


## run.py

Данный файл содержит основную логику программы - определение объектов на веб-камере. 


### is_user_wants_quit

Данная функция не принимает параметров на вход. В качестве выходных данных программа может вернуть два возможных состояния ```True``` или ```False```.

В последствии, если функция вернет значение ```True```, то программа завершит свою работу.

Здесь, функция ```waitKey(1)``` ожидает нажатия любой клавиши с частотой обновления кадра не реже 1 мс. 

В случае, если была нажата клавиша, то вторым условием проверки будет сравнение данной клавиши с клавишей "q". 

Здесь используется ```0xFF```, т.к. при включенном и выключенном NumLock могут быть получены разные значения. Используя ```0xFF``` данная проблема решена.


### show_frame

Данная функция принимает на вход изображение для вывода на экран, и не имеет выходных параметров. 

Здесь выполняется функция ```cv2.imshow```, аргументами которой является имя окна для отображения и само изображение. 

Благодаря данной функции происходит вывод данных веб-камеры на экран.


### draw_sqare
  
Данная функция принимает на вход изображение для вывода на экран и цвет рамки в цветовом пространстве RGB для выделения обнаруженого  объекта.
  
Функция не имеет выходных параметров. 

Её основная задача - прорисовка прямоугольника обнаруженного классификатором объекта с помощью функции ```cv2.rectangle```. 

В качестве аргументов, мы передаем ```cv2.rectangle``` следующие значения: 

* Изображение;
* Начальные координаты x,y;
* Конечные координаты x,y;
* Цвет рамки;
* Толщина линии границы прямоугольника в пикселях.


### get_cascades

Данная функция не принимает никаких входных параметров. В качестве выходных данных программа возвращает список, который в ключает в себя пары следующего вида: (загруженный файл xml-классификатора, цвет рамки в цветовом пространстве RGB для выделения обнаруженого  объекта)

Здесь выполняется обработка глобальной переменной ```CASCADES``` загруженной из файла ```config.py```. 

С помощью цикла программа проходит по всем элементам и добавляет в список загруженный c помощью функции ```cv2.CascadeClassifier``` классификатор и цвет рамки, если у ключа ```draw``` стоит значени ```True```


### main

Здесь выполняются основные функции программы. 

Изначально происходит обработка каскадов из файла ```config.py```.  Затем с помощью ```cv2.VideoCapture(0)``` происходит запуск нулевой камеры, т.е. веб-камеры. 

После этого программа входит в режим бесконечного цикла. 

Сперва проимходит проверка, работает ли камера, в противном случае прогрмма завершит свою работу. После этого программа считывает изображение и переводит его в серый цвет с помощью функции ```cv2.cvtColor``` и ее аргумента ```cv2.COLOR_BGR2GRAY``` для последующего поиска объектов на ней. 

После этого начинается цикл по каскадам, и определение классифцируемого объекта каскадом на изображении посредством функции ```detectMultiScale```. Дальше происходит цикл по найденым классификатором объектам с последующей отрисовкой рамки с помощью ```draw_sqare```. 

Когда цикл по всем каскадам завершится программа покажет полученное изображение на экране вызовом функции ```show_frame```.

Затем программа проверит не была ли нажата кнопка выхода из программы использовав is_user_wants_quit. Если нет, то цикл повторится, в противном случае бесконечный цикл на этом закончится. 

Перед завершением программа очистит потребовавшиеся программные и аппаратные ресурсы (```video_capture.release```) и закроет все окна открытые программой(```cv2.destroyAllWindows```)


## requirements.txt

Данный файл хранит необходимую для установки версию библиотеки ```OpenCV```.
