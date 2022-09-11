# 1TASK
given a number x, we want to find the number z for which z² is most nearly x.

package main

import (

    "fmt"
    
)
func Sqrt(x float64) float64 {

    z := 1.0
    
    for i := 1; i <= 10; i++ {
    
        z -= (z * z - x) / (2 * z)
	
		    l := z * z
		    
        fmt.Printf("i = %v, z = %v, pow_of_z = %v\n", i, z, l)
	
    }
    
    return z
    
}

func main() {

    fmt.Println("sqrt of 2 = ",Sqrt(2))
    
}


 в итоге мы получаем такой вывод. как мы видим,мы нашли число z, для которого z² наиболее близко к x(i = 2).
//i = 1, z = 1.5, z squared = 2.25
//i = 2, z = 1.4166666666666667, z squared = 2.0069444444444446
//i = 3, z = 1.4142156862745099, z squared = 2.000006007304883
//i = 4, z = 1.4142135623746899, z squared = 2.0000000000045106
//i = 5, z = 1.4142135623730951, z squared = 2.0000000000000004
//i = 6, z = 1.414213562373095, z squared = 1.9999999999999996
//i = 7, z = 1.4142135623730951, z squared = 2.0000000000000004
//i = 8, z = 1.414213562373095, z squared = 1.9999999999999996
//i = 9, z = 1.4142135623730951, z squared = 2.0000000000000004
//i = 10, z = 1.414213562373095, z squared = 1.9999999999999996
//sqrt of 2 =  1.414213562373095


# 2 TASK
change the loop condition to stop once the value has stopped changing 
 
package main
import (
    "fmt"
	  "math"
)
func Sqrt(x float64) float64 {
    z := 1.0
   	i := 0
    for x >= z {
        z -= (z * z - x) / (2 * z)
		i+=1
        fmt.Printf("i = %v,  z = %v\n ",i , z)
		if z == math.Sqrt(x) {
			break
		}
    }
    return z
}
func main() {
    fmt.Println("sqrt of 2 = ",Sqrt(2))
}

в итоге мы получаем такой вывод.
 //i = 1,  z = 1.5
 //i = 2,  z = 1.4166666666666667
 //i = 3,  z = 1.4142156862745099
 //i = 4,  z = 1.4142135623746899
 //i = 5,  z = 1.4142135623730951
 //sqrt of 2 =  1.4142135623730951
 
