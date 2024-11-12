# Quiz 018

![Captura de tela 2024-11-11 212516](https://github.com/user-attachments/assets/e312ff7c-24ff-4c47-951f-ffc8461802e6)


## Paper Work

![IMG_3842](https://github.com/user-attachments/assets/1b4ff0f6-add0-4578-8a01-56833622a40c)

## Code

```py
def function(A,B,C):
  ans = (A and B) or (not B) or not(C and B)
  if ans:
    print(f'| {A} | {B} | {C} |          1          |')
  else:
    print(f'| {A} | {B} | {C} |          0          |')

print('| A | B | C | AB + not B + not CB |')
for a in (0, 1):
  for b in (0, 1):
    for c in (0, 1):
      function(a,b,c)

```

## Proof of Work

![Captura de tela 2024-11-11 214002](https://github.com/user-attachments/assets/4887efb7-7111-47bb-9c6c-7842b327d7c7)

## Truth Table for X = ZW ⨁ (Z ⨁ Y(not W)) 

![IMG_3843](https://github.com/user-attachments/assets/06d28939-dcf6-482d-b213-d0461b13558d)


## Circuit for X = ZW ⨁ (Z ⨁ Y(not W)) 

![Captura de tela 2024-11-11 214022](https://github.com/user-attachments/assets/212bda78-c436-493d-bdef-eede33616d80)
