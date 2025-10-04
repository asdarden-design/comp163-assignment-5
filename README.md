# Anzino Darden
# COMP163 - Assignment 5

# Challenge 1: Collatz Sequence
print("=== Challenge 1: Collatz Conjecture ===")
current_number = int(input("Enter starting number: "))
step_count = 0

print("Sequence:", end=" ")

if current_number == 1:
    # Special case: already at 1
    print("1", end=" ")
else:
    while current_number != 1:
        print(current_number, end=" ")
        if current_number % 2 == 0:
            current_number = current_number // 2
        else:
            current_number = current_number * 3 + 1
        step_count += 1
    print(1, end=" ")  # print final 1

print()
print("Steps:", step_count)

Critical Thinking Q: Why use a while loop instead of a for loop?
Answer: Because we don’t know how many steps the Collatz sequence will take. A while loop continues until a condition is met (number = 1), but i for loop would require knowing the number of iterations in advance.

git add anzino_darden_assignment.py
git commit -m "Challenge 1: Collatz Conjecture - while loop for unknown iterations"

# Challenge 2: Prime Number Checker
print("\n=== Challenge 2: Prime Number Checker ===")
n = int(input("Enter a number: "))

print(f"Testing divisors from 2 to {n-1}...")

is_prime = True
for d in range(2, n):   # renamed to d
    if n % d == 0:
        print(f"{n} is not prime (divisible by {d})")
        is_prime = False
        break

if is_prime:
    print(f"{n} is prime!")

Critical Thinking Q: Why use a for loop instead of a while loop?
Answer: Because we know the exact range of divisors (2 to n-1). A for loop is ideal when the number of iterations is known in advance

git add anzino_darden_assignment.py
git commit -m "Challenge 2: Prime Number Checker - for loop for known ranges"

# Challenge 3: Multiplication Table Grid
print("\n=== Challenge 3: Multiplication Table ===")
print("Multiplication Table:")

# header row
print("   ", end="")
for j in range(1, 11):   # inner loop renamed to j
    print(f"{j:4}", end="")
print()

# table rows
for i in range(1, 11):   # outer loop renamed to i
    print(f"{i:2}", end="")
    for j in range(1, 11):
        value = i * j
        print(f"{value:4}", end="")
    print()

Critical Thinking Q: Why nested loops? Which should be outer vs inner?
Answer: Because we’re working with a grid (rows × columns). The outer loop goes through each row (1–10). The inner loop prints the row’s multiplication values across all columns (1–10).

git add anzino_darden_assignment.py
git commit -m "Challenge 3: Multiplication Table Grid - nested loops for 2D data"

# README

Challenge Explanations
Challenge 1: Collatz Conjecture
Loop Type: While loop
Reason: The number of steps is unknown until the sequence ends at 1.
How it works:
Repeatedly applies Collatz rules (divide if even, multiply by 3 and add 1 if odd).
Counts steps until reaching 1.
Challenge 2: Prime Number Checker
Loop Type: For loop
Reason: We know the exact range of divisors to test (2 to n-1).
How it works:
Checks each divisor in range.
Stops early if one divides evenly.
Challenge 3: Multiplication Table
Loop Type: Nested loops
Reason: One loop handles rows, another handles columns.
How it works: 
Outer loop each row from 1–10.
Inner loop prints row × column values.
AI Assistance:
Used chatgpt for concept clarification, formatting, placement of github commands for branching and debugging assistance.

git add README.md
git commit -m "Add loop design documentation"
