## Question
<img width="966" alt="Screen Shot 2024-09-09 at 9 34 10" src="https://github.com/user-attachments/assets/8c32b068-f16c-487e-a9af-a42f02c00190">

## Answer
```py

```


## Code running

# Quiz 073
## Question
<img width="953" alt="Screen Shot 2024-09-09 at 9 34 22" src="https://github.com/user-attachments/assets/de4dda9d-5522-485e-a1b6-aab66959ea51">

## Answer
```py

```
<img width="248" alt="Screen Shot 2024-09-09 at 9 40 37" src="https://github.com/user-attachments/assets/5f069bff-8007-436d-a379-356a3949cdf4">

<img width="373" alt="Screen Shot 2024-09-09 at 9 40 04" src="https://github.com/user-attachments/assets/5e9beff0-9cb9-4367-9617-6389cfb08f69">

## Code running

# Quiz074
## Question
<img width="955" alt="Screen Shot 2024-09-09 at 9 34 31" src="https://github.com/user-attachments/assets/0041fcb8-fd79-4b19-9782-9cba749c4e63">

## Answer
<img width="392" alt="Screen Shot 2024-09-09 at 9 38 13" src="https://github.com/user-attachments/assets/22ef57ca-5ba0-4ada-94bf-06ba25e8a11c">

## Code running


# Quiz 075
## Question
<img width="952" alt="Screen Shot 2024-09-09 at 9 34 47" src="https://github.com/user-attachments/assets/e1f77f05-b5b6-44c5-8dfb-edeaf4ecf026">

## Answer
```.py
import matplotlib.pyplot as plt
import numpy as np


def make(i):
    k = 0
    while 2**k < i+k+1:
        k += 1
    y = i / (k + i)
    plt.plot(i, y, marker='*', color="blue")

for i in range(1,1001):
    n = make(i)

plt.xlabel('n')
plt.ylabel("Efficiency")
plt.title('hamming code efficiency')
plt.legend()
plt.show()
```
<img width="462" alt="Screen Shot 2024-09-09 at 9 39 45" src="https://github.com/user-attachments/assets/5f278da0-f911-45d0-9b50-14c8adfc1b1c">

## Code running
<img width="359" alt="Screen Shot 2024-09-09 at 9 29 16" src="https://github.com/user-attachments/assets/acfa78d0-8481-47db-a36a-424b56387063">

# Quiz 076
## Question
<img width="956" alt="Screen Shot 2024-09-09 at 9 34 59" src="https://github.com/user-attachments/assets/90489f73-3ff0-42d5-a34a-5300d79c9ea9">

## Answer
```py

```
<img width="536" alt="Screen Shot 2024-09-09 at 9 40 58" src="https://github.com/user-attachments/assets/05b851a4-93c4-4af9-a0b2-72c006f186ff">

## Code Running

# Quiz 077
## Question
<img width="957" alt="Screen Shot 2024-09-09 at 9 36 16" src="https://github.com/user-attachments/assets/7b59e20a-bcfb-455c-a4ad-23899574ac89">

## Answer

# Quiz 078
## Question
<img width="968" alt="Screen Shot 2024-09-09 at 9 36 25" src="https://github.com/user-attachments/assets/7429a7ff-428f-4460-acdd-d8a0cd73104a">

## Answer
<img width="407" alt="Screen Shot 2024-09-09 at 9 41 57" src="https://github.com/user-attachments/assets/02672247-232d-4a9b-85b9-541910cc5424">

# Quiz 079
## Question
## Answer
'''.py
def msg(msg):
    msg = str(msg)
    n = len(msg)
    k = 0

    while 2**k < k + n + 1:
        k += 1

    new_msg_len = n + k
    position = [2**i - 1 for i in range(k)]
    total_msg = [-1] * new_msg_len
    j = 0
    for i in range(new_msg_len):
        if i not in position:
            total_msg[i] = int(msg[j])
            j += 1

    for i in range(k):
        parity_pos = 2**i - 1
        parity_sum = 0
        for j in range(parity_pos, new_msg_len, 2 * (parity_pos + 1)):
            parity_sum += sum(total_msg[j:j + parity_pos + 1])
        total_msg[parity_pos] = parity_sum % 2

    return total_msg

a = msg(1011)
print(a)
'''
<img width="407" alt="Screen Shot 2024-09-09 at 9 41 57" src="https://github.com/user-attachments/assets/02672247-232d-4a9b-85b9-541910cc5424">

## Code Running
<img width="438" alt="Screen Shot 2024-09-09 at 9 31 15" src="https://github.com/user-attachments/assets/ab6085ab-3621-4e47-b4d3-33b3c9d0fcc2">

