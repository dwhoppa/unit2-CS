# Quiz 019

![Captura de tela 2024-11-11 214244](https://github.com/user-attachments/assets/5f889b43-eb38-44f3-bfba-6513b3e4f327)

## Paper Work

![IMG_3855](https://github.com/user-attachments/assets/825544a7-87e3-461e-aebd-c85e4e54fdab)

## Code

```py
import random

def produce(n=5, m=3, s=2):
  random.seed(1234)
  x = []
  y = []
  for i in range(n):
    varia = random.randint(0,100)
    x.append(varia)
    y.append(varia**(0.5*(m/s)**2))
  print("|  x  |  y(x)  |")

  for i in range(n):
        print(f"|{x[i]:^6}|{y[i]:^8.2f}|")
        print("\n")
print(produce())

```

## Proof of Work

![Captura de tela 2024-11-12 030145](https://github.com/user-attachments/assets/dbdd43b5-1724-4be6-a025-ffd6bcc9175f)


## Truth Table for A(A+B) = A

![IMG_3857](https://github.com/user-attachments/assets/5e53ebcc-053a-45bb-b0e3-4c603374dfd7)




