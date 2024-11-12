# Quiz 023

![Captura de tela 2024-11-11 232632](https://github.com/user-attachments/assets/5c571c1c-41b2-4cf2-af11-2c7e4f010269)


## Paper Work


## Code 01

```py
from matplotlib import pyplot as plt

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0,
53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0,
50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0,
48.0, 48.0, 49.0]

spacing = 10/32
print(spacing)
spacing = int(spacing*10)
print(spacing)
x = []
for i in range(0,96,spacing):
  x.append(i/10)

print(len(x))

plt.plot(x,h)
plt.xlabel('time (minutes)')
plt.ylabel('relative humidity (%)')
plt.grid()
plt.show()

```

## Proof of Work for Code 1

![Captura de tela 2024-11-12 002446](https://github.com/user-attachments/assets/a3372c9a-51ce-40d8-b1de-e20a66bdbde4)

## Code 02

```py
from matplotlib import pyplot as plt

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0,
53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0,
50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0,
48.0, 48.0, 49.0]

spacing = 10/32
print(spacing)
spacing = int(spacing*10)
print(spacing)
x = []
for i in range(0,96,spacing):
  x.append(i/10)

print(len(x))


def mean(t):
  sum = 0;
  for i in t:
    sum += i

  return sum/len(t)

def linreg(x,y):

  x_m = mean(x)
  y_m = mean(y)

  print('x mean', x_m, '\ny mean', y_m)

  num = 0
  den = 0

  for i, j in zip(x,y):
      num += (i - x_m) * (j - y_m)
      den += (i - x_m) ** 2

  m = num/den

  b = y_m - m*x_m

  return m, b

m, b = linreg(x,h)

print(f"The H_model={m:.4f}*x+{b:.4f}")
```
## Proof of Work for Code 2

![Captura de tela 2024-11-12 010824](https://github.com/user-attachments/assets/4d23b09e-7970-4415-8489-9a74a9311222)

## b. Convert the following color hex to rgb
  #e6e627

    e6 = 1110 0110 = 128 + 64 + 32 + 4 + 2 = 230
    e6 = 230
    57 = 0101 0111 = 64 + 16 + 4 + 2 + 1 = 87
    #e6e627 = (230, 230, 87)
