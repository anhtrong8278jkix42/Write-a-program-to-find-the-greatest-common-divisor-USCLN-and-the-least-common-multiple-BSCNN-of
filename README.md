# Write-a-program-to-find-the-greatest-common-divisor-USCLN-and-the-least-common-multiple-BSCNN-of
Write a program to find the greatest common divisor (USCLN) and the least common multiple (BSCNN) of two positive integers a and b entered from the keyboard.
"""
  * Find the greatest common divisor (USCLN)
  *
  * @param a: positive integer
  * @param b: positive integer
  * @return USCLN of a and b
"""
def uscln(a, b):
     if (b == 0):
         return a;
     return uscln(b, a % b);
 
"""
  * Find the least common multiple (BSCNN)
  *
  * @param a: positive integer
  * @param b: positive integer
  * @return BSCNN of a and b
"""
def bscnn(a, b):
     return int((a * b) / uscln(a, b));
 
a = int(input("Enter a positive integer a = "));
b = int(input("Enter a positive integer b = "));
#calculate USCLN of a and b
print("Greatest common divisor of", a, "and", b, "is:", uscln(a, b));
#calculate BSCNN of a and b
print("Least common multiple of", a, "and", b, "is:", bscnn(a, b));
