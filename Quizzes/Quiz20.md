# Quiz 020

![Captura de tela 2024-11-11 221323](https://github.com/user-attachments/assets/7d6a3000-3f56-4c46-b000-c3ab2cc2a38d)

## Paper Work

![IMG_3847](https://github.com/user-attachments/assets/14027f38-5de9-4719-8c70-14844fb5785b)


## Code

```py
import random

def produce(n, m, s):
  random.seed(1234)
  x = []
  y = []
  for i in range(n):
    varia = random.randint(0,100)
    x.append(varia)
    y.append(varia**(0.5*(m/s)**2))
  return y , x

from matplotlib import pyplot as plt
y, x = produce(n=5, m=3, s=2)
plt.plot(x,y)
plt.show()
```

## Proof of Work

![Captura de tela 2024-11-11 222339](https://github.com/user-attachments/assets/b4f61faa-5962-4dc4-b282-86bee409f515)


## Truth Table

![IMG_3846](https://github.com/user-attachments/assets/fed7617c-7da8-42f2-b4aa-a72f0e5bfb82)

