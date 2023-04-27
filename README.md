# Checkpoint-Sorting-and-searching-algorithms
<!-- In this implementation, the for loop iterates over the array from the second element to the last element. For each iteration, the current element is set as the key variable and the index j is set to the previous index (i-1).

The while loop then iterates over the sorted sublist from right to left, comparing each element to the key and shifting the elements one position to the right until it finds the correct position to insert the key. The j counter is decremented at each iteration of the while loop until the correct position is found.

Finally, the algorithm inserts the key in its correct position by assigning it to arr[j+1], which is the position just after the last element that was shifted to the right. -->


def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key
    return arr
