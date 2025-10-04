# Anzino Darden
# COMP163 - Assignment 5
# Demonstrating while loops, for loops, and nested loops

# -------------------------
# Challenge 1: Collatz Sequence
# -------------------------
print("=== Challenge 1: Collatz Conjecture ===")
current_number = int(input("Enter starting number: "))
step_count = 0

print("Enter starting number:", end=" ")

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

# -------------------------
# Challenge 2: Prime Number Checker
# -------------------------
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

# -------------------------
# Challenge 3: Multiplication Table Grid
# -------------------------
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
        product = i * j
        print(f"{product:4}", end="")
    print()
