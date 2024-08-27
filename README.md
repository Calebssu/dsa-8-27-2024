# Notes

### Problem 1: Insertion Sort

##### JS
~~~
insertionSort(pairs) {
        let arr = [];
        let fArr = [];
        
        for(let i = 0; i < pairs.length; i++){
            arr.push(pairs[i].key)
        }

        arr.sort((a, b) => {
            return a - b
        })

        for(let i = 0; i < arr.length; i++){
            for(let o = 0; o < pairs.length; o++){
                if(pairs[o].key === arr[i]){
                    fArr.push(pairs[o])
                }
            }
        }
        console.log(fArr)
        return fArr;
    }
~~~

Disclaimer: this solution does not work on the actual neetcode. on 8-27-2024 Dj said that as long as you get the sorted result it's acceptable

### Problem 2: Reverse Linked List

##### JS
~~~
var reverseList = function(head) {
    let pre = null;
    let next = null;
    let current = head;

    while (current !== null) {
        next = current.next;
        current.next = pre;
        pre = current;
        current = next;
    }

    head = pre;
    return head;
};
~~~

### Big O

##### Problem 1

For problem one it would be Linear time complexity O(n) because the runtime is based off of how many indexes are in the array.

##### Problem 2

For problem two it would also be Linear time complexity O(n) because it searches and accesses a singly-linked list. Also, the runtime is based off of how long the list is.

### Quicksort

Quicksort is one of the fastest sorting algorithms. How it works is that it takes an array of values and then chooses one of them to be the pivot. The pivot element acts as the anchor for our code so if we had an array of numbers: 

~~~
let arr = [1, 9, 43, 29, 10, 7]
~~~

If the pivot element were 10, then the rest of the elements would sort themselves to be higher or lower than ten. Then it swaps the pivot to land between the lower and higher values. This process repeats unti the array is sorted properly.

### Dijkstra's Algorithm

Dijkstra's Algorithm is used to find the shortest path between two nodes(most of the time in a weighted graph). Finding the quickest path between two nodes manually would take a ton of time so using this algorithm speeds up the process.

##### Example:

An example of this algorithm being useful in a real world scenario would be navigation. Let's say you want to find the quickest way from your home to your workplace, driving every possible route to find the fastest would be time consuming. But if you use Dijkstra's algorithm to map out and use the nodes(in this case different locations on the map) to find the quickest route to work.