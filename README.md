# Huffman-Shannon_fan
## Aim:
To perform Huffman and Shannon-Fano for the source {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python.

## Tools Required:
python IDE with Numpy and Scipy

## Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
## Calculation:
![image](https://github.com/user-attachments/assets/22dba0d2-c6f1-471b-9517-2a86c744aaa9)
![image](https://github.com/user-attachments/assets/3865abac-2eb6-482b-9df5-5ca111091e0b)
![image](https://github.com/user-attachments/assets/e233669d-bdeb-457d-8393-cc2aab6d8e75)

## output:
![Screenshot 2025-03-29 084600](https://github.com/user-attachments/assets/e629a17a-3d57-450c-a0c6-55af5c3dc553)

## Results:
Thus for the given source Huffman and Shannon-Fan has been verified successfully.

