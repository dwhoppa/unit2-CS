# Quiz 021

![Captura de tela 2024-11-11 214728](https://github.com/user-attachments/assets/0d8015c0-0cba-4986-9f45-c80977b0db30)


## Paper Work

![IMG_3845](https://github.com/user-attachments/assets/45d08207-6fdb-44c1-a6f5-324d4506daf9)

## Code

```py
from matplotlib import pyplot as plt

x = []
for i in range(-100,101,2):
  x.append(i/10)

y =[]
for i in x:
  y.append(2*(i+5)**2)

plt.plot(x,y)
plt.xlabel('x')
plt.ylabel('$f(x) = 2(x+5)^2$')
plt.grid()
plt.show()
```
## "Advanced" Code using numpy

```py
from matplotlib import pyplot as plt

import numpy as np

x = np.linspace(-10,10,100)
y = 2*(x+5)**2

plt.plot(x,y)
plt.xlabel('x')
plt.ylabel('$f(x) = 2(x+5)^2$')
plt.show()

```

## Proof of Work for Code

![Captura de tela 2024-11-11 220554](https://github.com/user-attachments/assets/91865e9a-649b-4d9c-97ee-72ddf0a0469d)

## Proof of Work for "Advanced" Code

![Captura de tela 2024-11-11 220827](https://github.com/user-attachments/assets/e62cd25b-19e3-410c-add8-811ef00f6456)

## Circuit for not(bit0 bit1 + not (bit0 + bit1))

![Captura de tela 2024-11-11 220957](https://github.com/user-attachments/assets/b18fea3c-c080-4e72-9830-c2e226096922)
