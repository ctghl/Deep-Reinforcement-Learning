
# Отчет 1. Исследование метода кросс-энтропии в среде Cartpole 

## 1.
При начальном значении `hidden_state=64` сходимость достигается в среднем за 43 итерации (от 34 до 52). 
Графики функции потерь и среднего вознаграждения приведены ниже. 


При увеличении значения `hidden_state=128` сходимость достигается в среднем за 48 итераций (от 20 до 75). 
Можно сделать вывод, что увеличение числа скрытых нейронов отрицательно влияет на скорость сходимости агента. 
Графики функции потерь и среднего вознаграждения приведены ниже. 



При уменьшении значения `hidden_state=32` сходимость достигается в среднем за 61 итерацию (от 45 до 76). 
Можно сделать вывод, что уменьшение числа скрытых нейронов также отрицательно влияет на скорость сходимости агента. 
Графики функции потерь и среднего вознаграждения приведены ниже. 



## 2.
Архитектура имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
Значение `hidden_size=64`. 

<img src="imgs/64seg.png"/>

Архитектура имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
Значение `hidden_size=64`. 


Архитектура имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, hidden_size)
nn.ReLU(),
nn.Linear(hidden_size, hidden_size)
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
Значение `hidden_size=64`. 

<img src="imgs/2sloya.png"/>

## 3. Видео отчет (2 балла)
Лучший результат показала архитектура, которая имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, hidden_size)
nn.ReLU(),
nn.Linear(hidden_size, hidden_size)
```
Значение `hidden_size=64`. 





