# DATE:
# EXP NO:7 
# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
# Program to search the item in a list using linear search.
# Developed by : MUKESH.B
# RegisterNumber : 212223230128
def linear_search(array,n,k):
    for i in range(0,k):
        if n==array[i]:
            return i
    return -1
array=eval(input())
n=eval(input())
array.sort()
k=len(array)
result=linear_search(array,n,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
# Program to find the element in a list using Binary Search(Iterative Method).
# Developed by : MUKESH.B
# RegisterNumber : 212223230128
def binary_search(array,n,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==n:
            return mid
        elif array[mid]>n:
            high=mid-1
        else:
            low=mid+1
    return -1
array=eval(input())
n=eval(input())
array.sort()
result=binary_search(array,n,0,len(array)-1)
if(result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)








```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

# Program to find the element in a list using Binary Search(recursive Method).
# Developed by : MUKESH.B
# RegisterNumber : 212223230128
def binarysearch(array,k,low,high):
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return binarysearch(array,k,low,mid-1)
        else:
            return binarysearch(array,k,mid+1,high)
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarysearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)







```
## Sample Input and Output

i)	#Use a linear search method to match the item in a list.
![Screenshot 2024-10-07 000123](https://github.com/user-attachments/assets/dbd60e98-d612-4bda-bd3a-7e2a55a7006f)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-10-07 000130](https://github.com/user-attachments/assets/90a8a74b-c2ad-4b0d-8a15-758ad9506c01)


iii)	# Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-10-07 000136](https://github.com/user-attachments/assets/1ed57b1f-4df5-4d08-8173-3f06c1c20372)







## Result
Thus the linear search and binary search algorithm is implemented using python programming.
