# [7. Reverse Integer](https://leetcode.com/problems/reverse-integer)

[中文文档](/solution/0000-0099/0007.Reverse%20Integer/README.md)

## Description

<p>Given a 32-bit signed integer, reverse digits of an integer.</p>

<p><strong>Example 1:</strong></p>

<pre>

<strong>Input:</strong> 123

<strong>Output:</strong> 321

</pre>

<p><strong>Example 2:</strong></p>

<pre>

<strong>Input:</strong> -123

<strong>Output:</strong> -321

</pre>

<p><strong>Example 3:</strong></p>

<pre>

<strong>Input:</strong> 120

<strong>Output:</strong> 21

</pre>

<p><strong>Note:</strong><br />

Assume we are dealing with an environment which could only store integers within the 32-bit signed integer range: [&minus;2<sup>31</sup>,&nbsp; 2<sup>31&nbsp;</sup>&minus; 1]. For the purpose of this problem, assume that your function returns 0 when the reversed integer overflows.</p>

## Solutions

<!-- tabs:start -->

### **Python3**

```python
class Solution:
    def reverse(self, x: int) -> int:
        y = int(str(abs(x))[::-1])
        res = -y if x < 0 else y
        return 0 if res < -2**31 or res > 2**31 -1 else res
```

### **Java**

```java
class Solution {
    public int reverse(int x) {
        long res = 0;
        while (x != 0) {
            res = res * 10 + (x % 10);
            x /= 10;
        }
        return res < Integer.MIN_VALUE || res > Integer.MAX_VALUE ? 0 : (int) res;
    }
}
```

### **...**

```

```

<!-- tabs:end -->
