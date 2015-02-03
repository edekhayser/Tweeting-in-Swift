# Tweeting-in-Swift
Tweet-sized bits of Swift code that perform useful functions

    let array: [Double] = [1,2,4,5,6,6,7,24,24,24,62,624]

Average (Arithmetic Mean) of Array
-------------------------------------

    let average = array.reduce(0.0, combine: +) / Double(countElements(array))
    println(average)      //"65.75"

Median of Sorted Array
-------------------------

    let len = countElements(array)
    let median = len % 2 == 0 ? (array[len/2] + array[len/2+1]) / 2 : array[len / 2]
    println(median)       //"15.5"
