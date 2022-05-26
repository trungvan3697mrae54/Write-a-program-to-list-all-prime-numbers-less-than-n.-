# Write-a-program-to-list-all-prime-numbers-less-than-n.-
Write a program to list all prime numbers less than n. Positive integer n is entered from the keyboard
import math
 
"""
  * check the original
  *
  * @author viettuts.vn
  * @param n: so nguyen duong
  * @return true is so nguyen so,
  * false is not original
"""
def isPrimeNumber(n):
     # n < 2 does not have to be a prime
     if (n < 2):
         return False;
 
     # check so nguyen to when n >= 2
     squareRoot = int(math.sqrt(n));
     for i in range(2, squareRoot + 1):
         if (n % i == 0):
             return False;
     return True;
 
n = int(input("Enter a positive integer n = "));
print("All primes less than", n, "are:");
sb = "";
if (n >= 2):
     sb = sb + "2" + " ";
for i in range (3, n+1):
     if (isPrimeNumber(i)):
         sb = sb + str(i) + " ";
     i = i + 2;
print(sb);
