
# Отчет 1. Исследование метода кросс-энтропии в среде Cartpole 

## 1.
При начальном значении `hidden_state=64` сходимость достигается в среднем за 45 итерации (от 25 до 65). 
Графики функции потерь и среднего вознаграждения приведены ниже. 


![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/fad1a567-7c25-4726-ad07-84df4a3ef464)
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/a4771782-5ea7-4cbb-adb2-e03a02156f18)

При увеличении значения `hidden_state=128` сходимость достигается в среднем за 53 итераций (от 45 до 65). 
Можно сделать вывод, что увеличение числа скрытых нейронов отрицательно влияет на скорость сходимости агента. 
Графики функции потерь и среднего вознаграждения приведены ниже. 

![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/e123f218-9fa6-484d-8bf9-065013e76985)
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/88378198-9d99-4884-bb62-27e277be24a3)


При уменьшении значения `hidden_state=32` сходимость достигается в среднем за 35 итераций (от 25 до 50). 
Можно сделать вывод, что уменьшение числа скрытых нейронов положительно влияет на скорость сходимости агента. 
Графики функции потерь и среднего вознаграждения приведены ниже. 
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/a5609887-28c4-476e-81a4-80a85c37bc34)

![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/8237b0ef-2259-4d56-a4df-98c147398a3a)


## 2.
Архитектура имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
Значение `hidden_size=64`. 
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/0ac450a1-ac7b-4565-b51b-b1a5012aede9)

![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/e5164a30-38c5-4a96-b624-cc7100d41d9c)

Архитектура имеет следующий вид: 
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
Значение `hidden_size=64`. 
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/9e942588-fc5b-4e10-840b-8d9c3c02dc1d)
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/3a0e2d7c-4448-49dd-9cb0-6ec8d3b4eda1)


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
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/8497737c-a199-47db-a424-58f378ee4482)
![image](https://github.com/ctghl/Deep-Reinforcement-Learning/assets/87769076/5b0b7e69-8cf2-443c-a3bb-0797e20080ae)


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

report_1.md
![video](https://github.com/ctghl/Deep-Reinforcement-Learning/blob/main/video/rl-video-episode-0.mp4)

