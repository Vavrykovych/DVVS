# DVVS
Merge of two arrays(python):

import numpy as np
import random 
import math

arr1 = []
arr2 = []
lena1 = int(input("Enter number of elements 1: "))
lena2 = int(input("Enter number of elements 2: "))
lb = int(input("Enter lower bound: "))
hb = int(input("Enter higher bound: "))
arr1 = [random.randint(lb, hb) for iter in range(lena1)]
arr2 = [random.randint(lb, hb) for iter in range(lena2)]
arr1.sort()
arr2.sort()
print(arr1)
print(arr2)

c = []
for i in range(len(arr1)+ len(arr2)-1):
    if arr1[i] >= arr2[i]:
        c.append(arr2[i])
        arr1.insert(0,0)
    else:
        c.append(arr1[i])
        arr2.insert(0,0)


c.append(max(arr1.pop(), arr2.pop()))
print(c)
