<details> <summary>Question 4: The provided code stub reads an integer, `n`, from STDIN. For all non-negative integers `i < n`, print `i²`.
Example: If n = 3, the list of non-negative integers that are less than n = 3 is [0, 1, 2]. Print the square of each number on a separate line.

Input Format: The first and only line contains the integer, n.

Sample Input 0:

Copy code
```
5
```
Sample Output 0:

```
0
1
4
9
16
```
</summary>
Answer:
# `code : 1`
```python
if __name__ == '__main__':
    n = int(input())
    for i in range(n):
        print(i * i)
```
# `code : 2`
```python
if __name__ == '__main__':
    n = int(input())
    for i in range(n):
        print(i * i)
```
</details>