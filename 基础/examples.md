> 寻找水仙花数
```Python
for num in range(100, 1000):
    low = num % 10
    mid = num // 10 % 10
    high = num // 100
    if num == low ** 3 + mid ** 3 + high ** 3:
        print(num)
```
> 反转正转数
```Python
num = int(input('num = '))
reversed_num = 0
while num > 0:
    reversed_num = reversed_num * 10 + num % 10
    num //= 10
print(reversed_num)
```
> 输出100以内的所有素数
```Python
import cmath
for i in range(2, 101):
    for j in range(2, int(cmath.sqrt(i).real + 1)):
        if (i % j) == 0:
            break
    else:
        print(i)
```
> 组合数
```Python
import math
res = math.factorial(100) // math.facotrial(10) // math.factorial(100-10)
```
>多参数
```Python
def sum(*args:int):
    total = 0
    for val in args:
        total += val 
    return total
```
>求最大公约数
```Python
def gcd(x:int, y:int) -> int:
    """求最大公约数"""
    (x, y) = (y, x) if x > y else (x, y)
    for factor in range(x, 0, -1):
        if x % factor == 0 and y % factor == 0:
            return factor