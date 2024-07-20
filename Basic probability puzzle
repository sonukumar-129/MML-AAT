import math

def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

def calculate_probability(W1, B1, W2, B2):
    numerator = W1 * B2 + B1 * (B2 + 1)
    denominator = (W1 + B1) * (W2 + B2 + 1)

    
    common_divisor = gcd(numerator, denominator)
    numerator //= common_divisor
    denominator //= common_divisor
    return numerator, denominator

try:
    W1 = 5
    B1 = 4
    W2 = 7
    B2 = 6

    if W1 < 0 or B1 < 0 or W2 < 0 or B2 < 0:
        raise ValueError("Number of balls cannot be negative.")

    numerator, denominator = calculate_probability(W1, B1, W2, B2)

    print(f"{numerator}/{denominator}")

except ValueError as e:
    print(f"Invalid input: {e}")
