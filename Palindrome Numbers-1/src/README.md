# Palindrome Checker

This Java program checks whether a given integer is a palindrome or not. A palindrome is a number that reads the same backward as forward.

## Usage

The `isPalindrome` method takes an integer as input and returns `true` if it is a palindrome, and `false` otherwise. If the input is negative, the method returns `false` since negative numbers cannot be palindromic.

```java
public class Solution {
    public static boolean isPalindrome(int x) {
        if (x < 0) {
            return false;
        }

        int original = x;
        int reversed = 0;

        while (x != 0) {
            reversed = (reversed * 10) + (x % 10);
            x /= 10;
        }

        return original == reversed;
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome(121));   // true
        System.out.println(isPalindrome(-121));  // false
        System.out.println(isPalindrome(10));    // false
    }
}
