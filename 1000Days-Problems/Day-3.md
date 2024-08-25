<details> <summary>Question 3: The provided code stub reads two integers, `a` and `b`, from STDIN. Add logic to print two lines:
The first line should contain the result of integer division, a // b.
The second line should contain the result of float division, a / b.
No rounding or formatting is necessary.

Example: If a = 3 and b = 5:

The result of the integer division 3 // 5 = 0.
The result of the float division is 3 / 5 = 0.6.
Print:

Copy code
0
0.6
Input Format:

The first line contains the first integer, a.
The second line contains the second integer, b.
Output Format: Print the two lines as described above.

Sample Input :
```
4
3
```
Sample Output :
```
1
1.33333333333
```
</summary>
Answer:

```python
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a // b)
    print(a / b)
```
</details>

