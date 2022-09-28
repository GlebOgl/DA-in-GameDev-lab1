# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил(а):
- Оглоблин Глеб Александрович
- РИ210941
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.

## Цель работы
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### Hello World на Python и Unity
![image](https://user-images.githubusercontent.com/79518116/192587228-34c4bfcf-5597-44b6-bc25-c150c77e48d9.png)
![image](https://user-images.githubusercontent.com/79518116/192587486-dc00b672-1acc-4a1c-8137-3673dca26472.png)
![image](https://user-images.githubusercontent.com/79518116/192587562-19c14e5f-bbfb-4426-8595-f54b1e30742e.png)
![image](https://user-images.githubusercontent.com/79518116/192587675-44e4bbb4-0aab-4e56-97cd-1729567f5018.png)



## Задание 2
### Пошагово выполнить каждый пункт раздела "ход работы" с описанием и примерами реализации задач
Ход работы:
- Произвести подготовку данных для работы с алгоритмом линейной регрессии. 10 видов данных были установлены случайным образом, и данные находились в линейной зависимости. Данные преобразуются в формат массива, чтобы их можно было вычислить напрямую при использовании умножения и сложения.
2.1

```py

In [ ]:
#Import the required modules, numpy for calculation, and Matplotlib for drawing
import numpy as np
import matplotlib.pyplot as plt
#This code is for jupyter Notebook only
%matplotlib inline

# define data, and change list to array
x = [3,21,22,34,54,34,55,67,89,99]
x = np.array(x)
y = [2,22,24,65,79,82,55,130,150,199]
y = np.array(y)

#Show the effect of a scatter plot
plt.scatter(x,y)

```
![image](https://user-images.githubusercontent.com/79518116/192839375-bdeb99ab-5c41-42ad-b9df-f5971cd9d810.png)

2.2
- Определите связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: метод градиентного спуска для нахождения частных производных w и b.

![image](https://user-images.githubusercontent.com/79518116/192843057-397f4279-bc3f-4117-9a40-6e3f71aca199.png)

2.3
-Начать итерацию
![image](https://user-images.githubusercontent.com/79518116/192843923-4921f27a-2f4d-4e5d-9101-302f6858a006.png)

![image](https://user-images.githubusercontent.com/79518116/192844308-49806504-f543-41de-a400-1622d7411f5d.png)

![image](https://user-images.githubusercontent.com/79518116/192844464-15778c68-1320-4070-94cb-7fcbb1834f5c.png)

![image](https://user-images.githubusercontent.com/79518116/192844581-bb2898b8-4753-41a9-9dbb-801054e2c662.png)

![image](https://user-images.githubusercontent.com/79518116/192844703-8fc00bea-2280-4207-8aef-22e1893d8a43.png)

![image](https://user-images.githubusercontent.com/79518116/192844793-193a3579-0255-4b1c-bbb1-af25bda0362b.png)


## Задание 3
### Должна ли величина loss стремиться к нулю при изменении исходных данных? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ.

-loss это разница между предсказаным значением и настоящим, при увеличении количества итераций loss становится меньше тк настоящее и предсказаное значение становятся ближе друг к другу, следовательно при бесконечном количестве итераций loss будет стремиться к 0
![image](https://user-images.githubusercontent.com/79518116/192847802-f52ba610-0ffb-4ded-80f7-b0b1e527af80.png)

![image](https://user-images.githubusercontent.com/79518116/192847872-d2410832-f182-4ba3-93e7-1fa18a88347c.png)


```

## Задание 4
### Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.

- lr точность с которой высчитывается функция, чем меньше значение lr тем ближе предсказанное значение  к настоящему, но тем больше итераций необходимо для вычисления точного значения
(меняется loss)

![image](https://user-images.githubusercontent.com/79518116/192849263-8382fef0-8331-49a5-8883-7bed4f181155.png)
![image](https://user-images.githubusercontent.com/79518116/192849589-20449eb4-4e9d-48ac-b812-952042839351.png)

```py

import ScriptEnv
ScriptEnv.Initialize("Ansoft.ElectronicsDesktop")
oDesktop.RestoreWindow()
oProject = oDesktop.NewProject()
oProject.Rename("C:/Users/denisov.dv/Documents/Ansoft/SphereDIffraction.aedt", True)
oProject.InsertDesign("HFSS", "HFSSDesign1", "HFSS Terminal Network", "")
oDesign = oProject.SetActiveDesign("HFSSDesign1")
oEditor = oDesign.SetActiveEditor("3D Modeler")
oEditor.CreateSphere(
	[
		"NAME:SphereParameters",
		"XCenter:="		, "0mm",
		"YCenter:="		, "0mm",
		"ZCenter:="		, "0mm",
		"Radius:="		, "1.0770329614269mm"
	], 
)

```

## Выводы

Абзац умных слов о том, что было сделано и что было узнано.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
