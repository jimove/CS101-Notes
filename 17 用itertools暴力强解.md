# 用itertools暴力强解  
-----

## combinations: 返回不重复的所有组合  
```py
import itertools
a = [ 1,2,3,4 ]
for x in itertools.combinations( a,2 ):
    print( x )    
```
```py
(1, 2) (1, 3) (1, 4) (2, 3) (2, 4) (3, 4)
```  
-----  
##product: 等于两个for循环
```py
import itertools
for x in itertools.product([ 1,2,3,4 ], [ ’g’,’h’,’i’ ]):
    print( x )
```
```py
(1, ’g’) (1, ’h’) (1, ’i’) (2, ’g’)...(4, ’i’)
```
也可以用`repeat`属性对同一个序列进行迭代
```py
import itertools
for x in itertools.product( [ 1,2,3,4 ], repeat=3 ):
    print( x )
```
```py
(1, 1, 1) (1, 1, 2) (1, 1, 3) (1, 1, 4) (1, 2, 1) ...
```
-----
