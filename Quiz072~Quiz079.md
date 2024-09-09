## Question

<img width="966" alt="Screen Shot 2024-09-09 at 9 34 10" src="https://github.com/user-attachments/assets/8c32b068-f16c-487e-a9af-a42f02c00190">

## Answer

<img width="395" alt="Screen Shot 2024-09-09 at 20 08 30" src="https://github.com/user-attachments/assets/1dfa2414-5d5b-49dc-8d2a-c79b986a415d">

# Quiz 073
## Question

<img width="953" alt="Screen Shot 2024-09-09 at 9 34 22" src="https://github.com/user-attachments/assets/de4dda9d-5522-485e-a1b6-aab66959ea51">

## Answer
```py

def recieve(msg):
    if len(msg)%3 != 0:
        print("message invalid")
    length = len(msg)//3
    one = msg[0:length]
    two = msg[length:2*length]
    three=msg[length*2:3*length]
    if one == two:
        if two == three:
            print(msg, 'False')
        else:
            print('True')
            print(f"{one}{two}{three}")
    else:
        print('True')
        if two==three:
            print(f"{two}{two}{three}")
        elif one == three:
            print(f"{one}{one}{three}")
        else:
            print("message invalid")

a = recieve('100111001011001110010110011100101')
print(a)

b=recieve('011101111101110111110111001111')
print(b)


```

<img width="373" alt="Screen Shot 2024-09-09 at 9 40 04" src="https://github.com/user-attachments/assets/5e9beff0-9cb9-4367-9617-6389cfb08f69">

## Code running

<img width="457" alt="Screen Shot 2024-09-09 at 20 17 59" src="https://github.com/user-attachments/assets/0d89b3da-3d23-4ccd-9a31-6f11620d3ed9">

# Quiz074
## Question

<img width="955" alt="Screen Shot 2024-09-09 at 9 34 31" src="https://github.com/user-attachments/assets/0041fcb8-fd79-4b19-9782-9cba749c4e63">

## Answer
```.py
def counter(input):
    ones =0
    count=0
    for i in range(1,len(input)):
        if count != 0:
            if i ==1:
                ones += 1
                count +=1
    if count %2 ==0:
        if input[0]==1:
            message = "True"
        else:
            message = "False"
    else:
        if input[0] ==0:
            message ="True"
        else:
            message="False"
    print(message)

a = counter('100110001011001110010110011100101')
print(a)
b = counter('011101111101110111110111001111')
print(b)
```

<img width="392" alt="Screen Shot 2024-09-09 at 9 38 13" src="https://github.com/user-attachments/assets/22ef57ca-5ba0-4ada-94bf-06ba25e8a11c">

## Code running

<img width="191" alt="Screen Shot 2024-09-09 at 20 27 17" src="https://github.com/user-attachments/assets/06651324-847a-4eec-9046-b9476a55181c">

(The answer of the quiz is wrong as the first row has even numbers and starts with 1 and the second row has odd numbers and starts with 0 which makes both true)
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

## Code Running

# Quiz 077
## Question

<img width="957" alt="Screen Shot 2024-09-09 at 9 36 16" src="https://github.com/user-attachments/assets/7b59e20a-bcfb-455c-a4ad-23899574ac89">

## Answer
```.py
def get_parity(k,p):
    msg=""
    num = 0
    for i in range(1,k):
        new=2**p
        if new & p ==1:
            msg+=f'{new-1}'
        num+=1
a= get_parity(7,1)
print(a)
b=get_parity(7,2)
print(b)
c=get_parity(7,3)
print(c)

```
<img width="536" alt="Screen Shot 2024-09-09 at 9 40 58" src="https://github.com/user-attachments/assets/05b851a4-93c4-4af9-a0b2-72c006f186ff">

## Code Running

<img width="192" alt="Screen Shot 2024-09-09 at 14 41 22" src="https://github.com/user-attachments/assets/68634091-8013-47ca-beed-3291bab4b54b">

# Quiz 078
## Question

<img width="968" alt="Screen Shot 2024-09-09 at 9 36 25" src="https://github.com/user-attachments/assets/7429a7ff-428f-4460-acdd-d8a0cd73104a">

## Answer

<img width="407" alt="Screen Shot 2024-09-09 at 9 41 57" src="https://github.com/user-attachments/assets/02672247-232d-4a9b-85b9-541910cc5424">

# Quiz 079
## Question
## Answer
```.py
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
```

<img width="407" alt="Screen Shot 2024-09-09 at 9 41 57" src="https://github.com/user-attachments/assets/02672247-232d-4a9b-85b9-541910cc5424">

## Code Running

<img width="438" alt="Screen Shot 2024-09-09 at 9 31 15" src="https://github.com/user-attachments/assets/ab6085ab-3621-4e47-b4d3-33b3c9d0fcc2">

