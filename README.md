# Notes

### Problem 1: Insertion Sort

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

