# DSL-5
# Practical no 06 
# Problem Statement: Write a python program to store first year percentage of students in array. Write function for sorting array of floating point numbers in ascending order using 
# a) Selection Sort 
# b) Bubble sort and display top five scores
# program:-
def selection_short(L):
   n=len(L)
   for i in range(n):
     
     for j in range(i+1,n):
       if(L[j]<L[i]):
          
          L[i],L[j]=L[j],L[i]
   print(L,"\n")
   print("---------------")
   #return L
   
def bubble_short(L):
   n=len(L)
   
   for i in range(n):
      
      for j in range(0,n-i-1):
         
         if(L[j]>L[j+1]):
            
           L[j+1],L[j]=L[j],L[j+1]
   print(L,"\n")
   print("---------------")
   #return L


def inserction_short(L):
    n=len(L)
    
    for i in range(1,n):
       j=i
       while(L[j-1]>L[j])and(j>0):
          L[j-1],L[j]=L[j],L[j-1]
          j-=1
    print(L,"\n")
    print("---------------")




l=[]
n=int(input("Enter the no of elements : "))
for i in range(n):
   x=int(input("enter value :  "))
   l.append(x)
print("your list is : ",l)
      
while True:
   print()
   print("1:SELECTION SHORT ")
   print("2:BUBBLE SHORT ")
   print("3:INSERTION SHORT ")
   print("4:EXIT ")
   ch=int(input("ENter Your Choice : "))
   
   if ch==1:
        print("\nSELECTION SHORT \n")
        selection_short(l)
   elif ch==2:
        print("\nBUBBLE SHORT \n")
        bubble_short(l)
   elif ch==3:
        print("\nINSERCTION SHORT ")
        inserction_short(l)
   elif ch==4:
        False
   else:
       print("invalid choice ")

# Output:
# Enter the no of elements : 6
# enter value :  22
# enter value :  66
# enter value :  11
# enter value :  88
# enter value :  29
# enter value :  77
# your list is :  [22, 66, 11, 88, 29, 77]

# 1:SELECTION SHORT 
# 2:BUBBLE SHORT 
# 3:INSERTION SHORT 
# 4:EXIT 
# ENter Your Choice : 1
# SELECTION SHORT
# [11, 22, 29, 66, 77, 88]
# ---------------

# 1:SELECTION SHORT
# 2:BUBBLE SHORT
# 3:INSERTION SHORT
# 4:EXIT
# ENter Your Choice : 2
# BUBBLE SHORT
# [11, 22, 29, 66, 77, 88]
# ---------------
# 1:SELECTION SHORT
# 2:BUBBLE SHORT
# 3:INSERTION SHORT
# 4:EXIT
# ENter Your Choice : 3
# INSERCTION SHORT
# [11, 22, 29, 66, 77, 88]
