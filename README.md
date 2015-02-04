# Tweeting-in-Swift
Tweet-sized bits of Swift code that perform useful functions

```swift
import Foundation

let array: [Double] = [5,1,7,21,62,77,1431,6,3,3]
```

Arithmetic Mean of Array
------------------------

```swift
/**
Arithmetic Mean
:param: a The array that the arithmetic mean will be found for.
:returns: The arithmetic mean of the input array.
*/
func aMean(a:[Double])->Double{
	return a.reduce(0.0,combine:+)/Double(countElements(a))
}   //161.6
```

Geometric Mean of Array
-----------------------

```swift
/**
Geometric Mean
:param: a The array that the geometic mean will be found for.
:returns: The geometric mean of the input array.
*/
func gMean(a:[Double])->Double{
	return pow(a.reduce(1.0,combine:*),1.0/Double(countElements(a)))
}   //13.9097817160872
```

Median of Array
-------------------------
```swift    
/**
Median
:param: a The array that the median will be found for.
:returns: The median of the input array.
*/
func med(var a:[Double])->Double{
	a.sort(<)
	let l = countElements(a)
	return l%2==0 ?(a[l/2]+a[l/2+1])/2:a[l/2]
}   //14.0
```
