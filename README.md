# library_matrix_mamdani

 
Нечёткий вывод используется для решения задач, где необходимо работать с нечеткими, невыразительными или неопределенными данными. Например, в задачах управления процессами, где точные математические модели могут быть слишком сложными. Нечеткий вывод позволяет работать с нечеткими данными и принимать решения на основе лингвистических переменных, которые не имеют четкого числового значения.


Библиотека позволяет:
•	использовать матричные нечёткие векторы, предикаты;
•	задавать входные и выходные параметры алгоритма;
•	задавать графики функций истинности предикатов выбором из заранее настроенного набора;
•	создавать правила базы знаний;
•	производить нечёткий логический вывод с использованием созданной базы знаний в соответствии с матричным алгоритмом или алгоритмом Мамдани.

1. Задание объекта класса FuzzyInferenceSystem.
Для начала работы вам нужно задать объект класса FuzzyInferenceSystem, который будет далее полностью описывать вашу систему.
Например: fis = FuzzyInferenceSystem()
2. Выбор алгоритма.
Для работы доступны два алгоритма – Мамдани и матричный. Для выбора алгоритма нужно присвоить полю algorithm соответствующее строковое значение.
Например: fis.algorithm = 'Matrix'или fis.algorithm = 'Mamdani'
3. Выбор метода получения четкого результата.
Для работы доступны два метода – метод центра тяжести масс и упрощенный метод дефаззификации. Для выбора метода нужно присвоить полю defuzzification соответствующее строковое значение.
Например: fis.defuzzification = "Simple" или fis.defuzzification = " Centroid"
Рекомендуется при выборе алгоритма Мамдани использовать метод Centroid, а для матричного – Simple.
4. Создание признака или лингвистической переменной.
Для этого нужно выбрать метод create_feature и передать ему 5 параметров: строковое значение с названием ЛП, строковое значение со системой измерения, значение типа float для указания минимального значения, значение типа float для указания максимального значения и логического значение, где true – входная переменная, а false – выходная.
Например: f_temp = fis.create_feature("Температура", "C", 0, 150, True)
