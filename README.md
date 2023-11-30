Program:
import pandas as pd
data = {"country": ["Brazil", "Russia", "India", "China", "South Africa"],
 "capital": ["Brasilia", "Moscow", "New Dehli", "Beijing", "Pretoria"],
 "area": [8.516, 17.10, 3.286, 9.597, 1.221],
 "population": [200.4, 143.5, 1252, 1357, 52.98]}
frame = pd.DataFrame(data)
print(frame)
print('------------------------------')
frame.index = ["BR", "RU", "IN", "CH", "SA"]

8.b
import numpy as np
# Creating a rank 1 Array
arr = np.array([1, 2, 3])
print("Array with Rank 1: \n",arr)
# Creating a rank 2 Array
arr = np.array([[1, 2, 3],[4, 5, 6]])
print("Array with Rank 2: \n", arr)
# Creating an array from tuple
arr = np.array((1, 3, 2))
print("\nArray created using ""passed tuple:\n", arr)

8.c
Program:
import matplotlib.pyplot as plt
# x axis value
x = [1,2,3]
# corresponding y axis values
y = [2,4,1]
# plotting the points
plt.plot(x, y)
# naming the x axis
plt.xlabel('x – axis')
# naming the y axis
plt.ylabel('y - axis')
# giving a title to my graph
plt.title('My first graph!')
# function to show the plot
plt.show()
8.d
from scipy import misc
import imageio
import matplotlib.pyplot as plt
# reads a raccoon face
face = misc.face()
# save the image
imageio.imsave('raccoon.png', face)
plt.imshow(face)
plt.show()

9.a
print("Enter the Name of Source File: ")
sFile = input()
print("Enter the Name of Target File: ")
tFile = input()
fileHandle = open(sFile, "r")
texts = fileHandle.readlines()
fileHandle.close()
fileHandle = open(tFile, "w")
for s in texts:
 fileHandle.write(s)
fileHandle.close()
print("\nFile Copied Successfully!")

9.b
print("Printing and count in text file")
file1=open("sample.txt", "r+")
wordcount={}
for word in file1.read().split():
 if word not in wordcount:
 wordcount[word]=1
 else:
 wordcount[word]=+1
sum=0
for k,v in wordcount.items():
 print(str(k)+ " – " +str(v))
 sum=sum+v
 print("Total number of words in file:",sum)
file1.close()
9.c
file1=open("sample.txt", "r")
str=file1.read()
word=str.split()
max_len=len(max(word,key=len))
for word in word:
 if(len(word)==max_len):
 longest_word=word
print("The longest word in file is:", longest_word)
10.a
a=int(input("Enter a number:"))
b=int(input("Enter a dividing number:"))
try:
 if(b==0):
 print("You cannot divide by zero!")
 else:
 print("The Division is:",a/b)
except ZeroDivisonError:
 print("Enter a valid number")
finally:
 print("Thankyou")

 10.b
 age=int(input("Enter your age:"))
try:
 if(age>18):
 print("Eligible to vote")
 else:
 print("Not Eligible to vote")
except:
 print("Enter a valid age")
finally:
 print("Thankyou")

 10.c

 mark=int(input("Enter your mark:"))
try:
 if(mark>=0):
 print("Your mark is:",mark)
 else:
 print("Enter a mark between 0 to 100")
except:
 print("Enter a valid input")
finally:
 print("Thankyou")

12
  import pygame
import time 
pygame.init()
screen=pygame.display.set_mode((500,300)) 
y=1
direction=1
counter=0
while True:
 screen.fill((255,255,255))
 pygame.draw.circle(screen,(0,255,0),(250,y),13,0)
 pygame.display.update()
 time.sleep(.008)
 if y==300:
 direction=-1
 elif y==0:
 direction=1
 counter=counter+1
 y=y+direction
 if counter==3:
 pygame.quit()
 break
 6.a
 def fact(n):
if n==0:
return 1
else:
return n*fact(n-1)
n=int(input("Enter the value of n:"))
print("The factorial is",fact(n))
