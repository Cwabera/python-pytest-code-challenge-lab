# lib/palindrome.py

def longest_palindromic_substring(s):
    if not isinstance(s, str):
        raise TypeError("Input must be a string")
    n = len(s)
    if n == 0:
        return ""
    
    start = 0
    max_length = 1
    
    for i in range(n):
        # Odd length palindrome
        l, r = i, i
        while l >= 0 and r < n and s[l] == s[r]:
            if r - l + 1 > max_length:
                start = l
                max_length = r - l + 1
            l -= 1
            r += 1
        
        # Even length palindrome
        l, r = i, i + 1
        while l >= 0 and r < n and s[l] == s[r]:
            if r - l + 1 > max_length:
                start = l
                max_length = r - l + 1
            l -= 1
            r += 1
    
    return s[start:start + max_length]