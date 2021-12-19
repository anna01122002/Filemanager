# Filemanager
---
## aka Тестирование файлового менеджера.

В данном Readme я постараюсь максимально информативно рассказать в процессе тестировки моего файлового менеждера, упомяну про трудности, особенности и фичи.

---
Итак, начнем с самого начала - создание проекта и применение библиотеки PyTest.

Изначально, я надеялась что обычное подключение библиотеки Pytest не сотавит труда. Но я ошиблась. Сама библиотека подключалась без ошибок, но вот выполения как ожидалось вот на этом фото не было:

![image](https://user-images.githubusercontent.com/71213226/144404286-6cd51f36-0860-4d5e-83aa-905f2400854b.png)

Прочитав достарочно много материала по использованию данной библиотеки, я убедилась, что просто подключить ее с нормальным функционалом не получится (разве что для самых простых тестов). 

Поэтому я использовала возможности PyCharm и подгрузила Pytest в конфигурацию проекта, назначив рабочую папку tests.
![image](https://user-images.githubusercontent.com/71213226/144398464-14358dc0-bd07-4b6e-a9c0-45cbfa134e8b.png)

Такой вариант действий немного упростил выполнение задачи.

## Основные элементы проекта
![image](https://user-images.githubusercontent.com/71213226/144399362-48376166-4c72-4852-ba18-4ee6ab5388f2.png)

**.pytast_cashe** - созданная библиотекой директория с лог файлами.

**tests** - директория, в которой находятся файлы с тестами, в нашем случае, для упрощения проверки  - 1 файл.

**util.py** - файл с самим файловым менеджером.


## Процесс тестировки

Сама логика реализации тестировки взята с **_лекции_**, то есть с использованием **фикстур**.

Всё с подробными комментариями описано в **tests/test_functions.py**/.

Разберем пример фикстуры и конкретного теста чтения файла:

  Фикстура:
  
  ![image](https://user-images.githubusercontent.com/71213226/144401234-de1c9718-ebb1-4e8b-9305-92c76b3f4f33.png)
  
  Тест:
  
  ![image](https://user-images.githubusercontent.com/71213226/144401332-73b502da-b531-4767-8583-6eac0d590338.png)

Логика проверки проста - выполнение того или иного действия фиксируется в самой программе на True или False, а тест сверяет значение с ожидаемым.

## Фича

В директории **.pytast_cashe** имеется файл nodeids следующего содержания:

![image](https://user-images.githubusercontent.com/71213226/144401772-70c78f86-8df2-40e9-927b-f514551d817e.png)

Тут описаны абсолютно все тесты в проекте, что упрощает проверку.

Как видно на скриншоте, выполнены все пункты задания.

На самом первом скриншоте в этом Readme указаны результаты тестов.

