<details>
  <summary>Question 1: 
Given an integer, n, perform the following conditional actions:
• If n is odd, print Weird
• If n is even and in the inclusive range of 2 to 5, print Not Weird
• If n is even and in the inclusive range of 6 to 20, print Weird
• If n is even and greater than 20, print Not Weird

**Input Format:**
A single line containing a positive integer, n.

**Constraints:**
• 1 ≤ n ≤ 100

**Output Format:**
Print "Weird" if the number is weird. Otherwise, print "Not Weird."

**Sample Input 0:**
3

**Sample Output 0:**
Weird

**Explanation 0:**
n = 3; n is odd, and odd numbers are weird, so print "Weird."

**Sample Input 1:**
24

**Sample Output 1:**
Not Weird

**Explanation 1:**
n = 24; n > 20 and n is even, so it is not weird.
</summary>
  
  **Answer:** 
  # `code 1`
```
if __name__ == '__main__':
    n = int(input().strip())
    if n in range(1,6):
        if n%2 == 0:
            print("Not Weird")
        else:
            print("Weird")
    elif n in range(5,21):
        if n%2 == 0:
            print("Weird")
        else:
            print("Not Weird")
    elif n in range(20,100):
        if n%2 == 0:
            print("Not Weird")
        else:
            print("Weird")
    else:
        print('Not Weird')
```
  # `code 2`
  ```
if __name__ == '__main__':
    n = int(input().strip())
    
    if n % 2 != 0:  # Odd numbers
        print("Weird")
    elif n % 2 == 0:
        if n in range(2, 6):  # Even and in range 2 to 5
            print("Not Weird")
        elif n in range(6, 21):  # Even and in range 6 to 20
            print("Weird")
        elif n > 20:  # Even and greater than 20
            print("Not Weird")
```
</details>
