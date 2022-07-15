def binarySearch (array, x, low, high):
    low = 0;
    
    mid = low
    index = -1
    while low < high :
        mid = low + (high - low) // 2
        if array[mid] > x :
            high = mid
        elif array[mid] < x :
            low = mid + 1
        else :
            index = mid
            high = mid
    return index
array = [4 ,5,2,4,5,6,2,3,4,5,7]
x = 4
new=sorted(array)
result = binarySearch(array, x, 0 , len(array) -1 )
print("Sorted Array is,",new)
if result != -1 : #If element is found
    print("Number of occurences of element",x,"is:",array.count(x))
else : #If element is not found
    print( "Not found" )