ADVANCED PYTHON TASK
people = [
    {'name': 'Alice', 'age': 22}, 
    
    {'name': 'Bob', 'age': 17},
    {'name': 'Charlie', 'age': 19}
]

# Filter people with age >= 18
adults = list(filter(lambda person: person['age']>= 18, people))
# Get only names
names = list(map(lambda person: person['name'], adults))
print(names)  # Output: ['Alice', 'Charlie'] 

question 02
from functools import reduce
numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 120

question 03
numbers = [1, 2, 3, 4, 5, 6]
is_even = lambda x: x % 2 == 0
squared_evens = [x ** 2 for x in numbers if is_even(x)]
print(squared_evens)  # Output: [4, 16, 36]

question 04
is_number = lambda s: s.replace('.', '', 1).isdigit() if s.count('.') <= 1 else False

print(is_number("123"))     # True
print(is_number("12.34"))   # True
print(is_number("abc"))     # False

question05
from functools import reduce
fibonacci = lambda n: reduce(lambda acc, _: acc + [acc[-1] + acc[-2]], range(n-2), [0, 1]) if n > 1 else [0]*n

print(fibonacci(10))  # Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
