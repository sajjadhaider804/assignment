
# Prime Number and Favorite Numbers Program

This program performs several operations based on user input of their favorite numbers:

- **Prime check**: A function to check if a number is prime.
- **User input**: Ask for the user's name and three favorite numbers.
- **Even/Odd check**: Determine if each favorite number is even or odd.
- **Square calculation**: Compute the square of each favorite number.
- **Sum calculation**: Calculate the sum of the three numbers and check if the sum is a prime number.

```python
def is_prime(n):
    """Check if a number is prime."""
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False
    return True

# 1. Prompt the user for their name
name = input("Enter your name: ")

# 2. Ask for three favorite numbers
numbers = []
numbers.append(int(input("Enter your first favorite number: ")))
numbers.append(int(input("Enter your second favorite number: ")))
numbers.append(int(input("Enter your third favorite number: ")))

# Greet the user
print(f"\nHello, {name}! Let's explore your favorite numbers:")

# 3. Determine even or odd for each number
even_odd_info = [(num, "even" if num % 2 == 0 else "odd") for num in numbers]
for num, even_odd in even_odd_info:
    print(f"The number {num} is {even_odd}.")

# 4. Calculate the square of each number and print it
print()
for num in numbers:
    print(f"The number {num} and its square: ({num}, {num**2})")

# 5. Calculate the sum of the numbers
total_sum = sum(numbers)
print(f"\nAmazing! The sum of your favorite numbers is: {total_sum}")

# 6. Check if the sum is a prime number
if is_prime(total_sum):
    print(f"Wow, {total_sum} is a prime number!")
else:
    print(f"The sum {total_sum} is not a prime number.")
```

