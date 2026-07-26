# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
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
# Calculation:

<img width="2115" height="3264" alt="pro-lL41OK9g" src="https://github.com/user-attachments/assets/772d27bd-e611-4e6d-8bcd-1349794c0955" />
<img width="1987" height="3264" alt="pro-V6hqkv7w" src="https://github.com/user-attachments/assets/5411b51d-972e-42bd-b253-0ed2f0ed2123" />
<img width="1449" height="924" alt="pro-9Kr8XDqc" src="https://github.com/user-attachments/assets/42427d06-9fde-452c-843d-f52176933e24" />



# Output

<img width="537" height="355" alt="image" src="https://github.com/user-attachments/assets/f20d2da3-45f2-4da8-a551-0334e550f1cc" />

 
# Results:

Huffman and Shannon-Fano coding methods were implemented on the provided source. Calculations for average codeword length, entropy, variance, redundancy, and coding efficiency have been carried out successfully

