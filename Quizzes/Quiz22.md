# Quiz 022

![Captura de tela 2024-11-11 230914](https://github.com/user-attachments/assets/c3d90071-d378-4b01-999e-598f084b1e0b)

## Paper Work + Convert FFA5


## Code

```py
from matplotlib import pyplot as plt

x = []
for i in range(-100,101,2):
  x.append(i/10)

y =[]
for i in x:
  y.append(abs(i))

from matplotlib import pyplot as plt

plt.plot(x,y)
plt.xlabel('x') 
plt.ylabel('$f(x) = |x|$')
plt.grid() 
plt.show()

```

## Proof of Work

![Captura de tela 2024-11-11 230815](https://github.com/user-attachments/assets/e8dd1ce5-9abc-4117-ba3d-d2ea9463dc9d)


## Convert FFA5

```py
x = [1,1,1,1, 1,1,1,1, 1,0,1,0 , 0,1,0,1]

sum = 0

for pos,value in enumerate(x):

  sum += value*2**(15-pos)

print(sum)
```
