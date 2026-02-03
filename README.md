# IS362-Generators-Iterables
IS362 week 2 assignment

Usage
-------
Generator functions allow you to declare a function that behaves like an iterator, i.e. it can be used in a for loop.

Link: [https://wiki.python.org/moin/Generators/](url)

Example
--------
# Generator Countdown 
def countdown(n): 
    """Count down from n to 1""" 
    print(f"Starting countdown from {n}") 
    while n > 0: 
        yield n 
        n -= 1 
    print("Lift off!") 
    
# Using the Generator
print("Example 1: Simple countdown")
for number in countdown(5):
    print(f"T-minus {number}...")

# Generators maintain state between yields
print("\nExample 2: Manual iteration")
counter = countdown(3)
print(next(counter))  
print(next(counter))  
print(next(counter))  

try:
    print(next(counter))  
except StopIteration:
    print("Generator exhausted!")

Output
