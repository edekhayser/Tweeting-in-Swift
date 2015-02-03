# Tweeting-in-Swift
Tweet-sized bits of Swift code that perform useful functions

Average (Arithmetic Mean) of [Double]
-------------------------------------

array.reduce(0.0, combine: +) / Double(countElements(array))

Median of Sorted [Double]
-------------------------

let len = countElements(array)
len % 2 == 0 ? (array[len/2] + array[len/2+1]) / 2 : array[len / 2]
