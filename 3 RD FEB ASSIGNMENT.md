Q1. Which keyword is used to create a function? Create a function to return a list of odd numbers in the
range of 1 to 25.
ANS: def keyword 
Q2. Why *args and **kwargs is used in some functions? Create a function each for *args and **kwargs to demonstrate their use.
ANS: args enable us to pass the variable number of non-keyword arguments to functions,kwargs allows us to pass any number of keyword arguments.
Q3. What is an iterator in python? Name the method used to initialise the iterator object and the method
used for iteration. Use these methods to print the first five elements of the given list [2, 4, 6, 8, 10, 12, 14,
16, 18, 20].
ANS: iter() method
Q4. What is a generator function in python? Why yield keyword is used? Give an example of a generator function.
ANS: Generaor Function is allows you to declare a function that behaves like an iterator, providing a faster and easier way to create iterators,yield keyword is used to create a generator function.
def test_fib1():
    a,b=1,2
    while True:
        yield a
        a,b = b, a+b
        fib = test_fib1()
        for i in range(12):
    print(next(fib))
     1 
     2
     3
     5
     8
     13
     21
     34
     55
     89
     144
     233
     
Q5. Create a generator function for prime numbers less than 1000. Use the next() method to print the first 20 prime numbers.
ANS: def primes():
    """Create a generator function for prime numbers less than 1000."""
    yield 2
    primes_list = [2]
    for i in range(3, 1000):
        is_prime = True
        for prime in primes_list:
            if i % prime == 0:
                is_prime = False
                break
        if is_prime:
            primes_list.append(i)
            yield i

prime_gen = primes()
# the next() method to print the first 20 prime numbers.
for i in range(20):
    print(next(prime_gen))

Q6. Write a python program to print the first 10 Fibonacci numbers using a while loop.?
ANS: ef test_fib1():
    a,b=1,2
    while True:
        yield a
        a,b = b, a+b
        fib = test_fib1()
        for i in range(10):
        1 
        2
        3
        5
        8
        13
        21
        34
        55
        89
       
Q8. Write a python program to check whether a given number is Palindrome or not using a while loop.
ANS:python program to check whether a given number is Palindrome or not using a while loop.
n = int(input("Please give a number : "))
def reverse(num):
    if num<10:
      return num 
    else:
      return int(str(num%10) + str(reverse(num//10)))
def isPalindrome(num):
    if num == reverse(num):
        return 1
    return 0
if isPalindrome(n) == 1:
    print("Given number is a palindrome")
else:
    print("Given number is a not palindrome") 

Q9. Write a code to print odd numbers from 1 to 100 using list comprehension.
ANS: a code to print odd numbers from 1 to 100 using list comprehension.
     [odd for odd in range(1,100) if odd%2!=0]
