
# Отчет 1. Исследование метода кросс-энтропии в среде Cartpole 

## 1.
При начальном значении `hidden_state=64` сходимость достигается в среднем за 45 итерации (от 25 до 65). 
Графики функции потерь и среднего вознаграждения приведены ниже. 

!([http://url/to/img.png](https://github.com/ctghl/Deep-Reinforcement-Learning/blob/main/Sem2/64_reward.png))

При увеличении значения `hidden_state=128` сходимость достигается в среднем за 53 итераций (от 45 до 65). 
Можно сделать вывод, что увеличение числа скрытых нейронов отрицательно влияет на скорость сходимости агента. 
Графики функции потерь и среднего вознаграждения приведены ниже. 



При уменьшении значения `hidden_state=32` сходимость достигается в среднем за 35 итераций (от 25 до 50). 
Можно сделать вывод, что уменьшение числа скрытых нейронов положительно влияет на скорость сходимости агента. 
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





