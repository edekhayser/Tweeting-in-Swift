# Tweeting-in-Swift
Tweet-sized bits of Swift code that perform useful functions.

```swift
import Foundation

let array: [Double] = [5,1,7,21,62,77,1431,6,3,3]
```

Arithmetic Mean of Array
------------------------

```swift
/**Arithmetic Mean

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
/**Geometric Mean

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
/**Median

:param: a The array that the median will be found for.
:returns: The median of the input array.
*/
func med(var a:[Double])->Double{
	a.sort(<)
	let l = countElements(a)
	return l%2==0 ?(a[l/2]+a[l/2+1])/2:a[l/2]
}   //14.0
```

Standard Deviation (Population)
-------------------------
```swift    
/**Standard Deviation (Population)

:param: a The array that the population standard deviation will be found for.
:returns: The population standard deviation of the input array.
*/
func σ(a:[Double])->Double{
	return pow(aMean(a.map{pow(($0-aMean(a)),2)}),0.5)
}   //406.614260724822
```

Standard Deviation (Sample)
-------------------------
```swift  
/**Standard Deviation (Sample)

:param: a The array that the sample standard deviation will be found for.
:returns: The sample standard deviation of the input array.
*/
func s(a:[Double])->Double{
	let b = a.map{pow(($0-aMean(a)),2)}
	return pow(b.reduce(0.0,combine:+)/Double(countElements(b)-1),0.5)
}   //426.460634440358
```	
