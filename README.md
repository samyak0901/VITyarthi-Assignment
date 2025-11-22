# VITyarthi-Assignment
This Repository contains all 34 questions of the assignment with code and reports.
ques2) Write a function digital_root(n) that repeatedly sums the digits of a number until a single digit is obtained.
WHAT WE DID-We developed a Python function, digital_root(n), to calculate the digital root of a given non-negative integer n. The primary implementation leverages a mathematical property of digital roots rather than a procedural loop of summing digits.
What We Learned:The "How Can It Help Others" section highlights that while a procedural (loop-based) method for calculating the digital root is straightforward, a more efficient, constant-time solution exists using the formula (n - 1) % 9 + 1 for all positive integers n. This mathematical shortcut provides a highly optimized way to solve the problem.
How Can It Help Others:This function is useful in various scenarios:
Checksum Verification: The digital root can serve as a simple checksum for verifying data integrity in basic systems.
Algorithmic Optimization: For software developers, the constant-time mathematical solution is significantly more performant than an iterative approach, especially when processing large numbers or performing the operation many times within a program.
Educational Tool: It serves as a clear example of how number theory and mathematical formulas can simplify and optimize programming tasks. 

ques6)Write a function is_deficient(n) that returns True if the sum of proper divisors of n is less than n.
What We Did:We created a Python function, is_deficient(n), that determines whether a given positive integer n is a deficient number. The function calculates the sum of all proper divisors of n (excluding n itself) and compares this sum to n.
What We Learned: We learned several mathematical and algorithmic concepts: Definition of Deficient Numbers: A number is deficient if the sum of its proper divisors is less than the number itself.Efficient Divisor Summation: The most efficient way to find all divisors is to iterate only up to the square root of n. For every divisor i found, its corresponding pair n // i is also a divisor. This significantly reduces the number of iterations compared to checking every number up to \(n/2\).Optimization with Early Exit: The function includes an optimization to return False as soon as the accumulating sum of divisors meets or exceeds n, avoiding unnecessary further calculations.
How Can It Help Others:
Number Theory Education: This function provides a practical example of classifying integers based on the properties of their divisors (deficient, perfect, or abundant).
Algorithmic Efficiency: The efficient implementation demonstrates best practices for optimizing loops involving divisor calculations, a common task in programming challenges and technical interviews.
Mathematical Research: It can be used as a building block in programs that analyze sequences of numbers or search for numbers with specific divisor properties.

ques12)Write a function is_prime_power(n) that checks if a number can be expressed as pᵏ where p is prime and k ≥ 1.
What We Did: We developed a Python function, is_prime_power(n), that determines if a given positive integer n can be expressed as a prime number raised to a positive integer power (\(p^{k}\), where \(p\) is prime and \(k\ge 1\)). The function works by finding the unique prime factors of n and checking if there is exactly one such factor.
What We Learned:
We learned a fundamental property of prime powers: they possess only one distinct prime factor in their unique prime factorization. The implementation uses an optimized trial division method, iterating only up to the square root of the remaining number to efficiently find these factors. We also included early exit conditions to immediately return False if a second distinct prime factor is discovered during the process.
How Can It Help Others:
Cryptography and Number Theory: The function is useful in algorithms that rely on the unique properties of prime powers, such as certain cryptographic protocols or number-theoretic research.
Algorithmic Thinking: It provides a clear demonstration of how to leverage the Fundamental Theorem of Arithmetic (every integer greater than 1 is either a prime number itself or can be represented as a unique product of prime numbers) to solve specific number classification problems efficiently.
Code Optimization: The implementation highlights practical optimization techniques, such as early termination and iterating only up to the square root, which are valuable skills for any programmer.

ques16)Write a function aliquot_sum(n) that returns the sum of all proper divisors of n (divisors less than n).
What We Did:
We developed a Python function, aliquot_sum(n), that efficiently calculates the sum of all proper divisors of a positive integer n (divisors excluding n itself).
What We Learned: Definition of Aliquot Sum: The function addresses a specific mathematical definition called the "aliquot sum" or "restricted divisor sum".Efficiency in Factor Finding: We learned that finding all divisors up to the square root of n is sufficient to find all divisor pairs. This optimization significantly reduces computational time compared to iterating through all numbers up to \(n/2\).Handling Edge Cases: Proper handling of edge cases, specifically n=1 (where the sum is 0) and perfect squares (where the square root is counted only once), is crucial for correctness.
How Can It Help Others:
Number Classification: This function is a fundamental building block for classifying numbers as deficient, perfect, or abundant (used in the earlier is_deficient function).
Mathematical Sequence Generation: It can be used to generate aliquot sequences, which are sequences of integers where each term is the aliquot sum of the previous term.
Algorithm Education: The code serves as a clear example of optimizing a loop that deals with divisors, a standard problem in introductory computer science and number theory applications.

ques21)Write a function Modular Multiplicative Inverse mod_inverse(a, m) that finds the number x such that (a * x) ≡ 1 mod m.
What We Did: We wrote a Python function mod_inverse(a, m) that computes the modular multiplicative inverse of a modulo m. The function utilizes the Extended Euclidean Algorithm to find an integer \(x\) such that \((a\times x)\equiv 1\quad (\mod m)\).
What We Learned: Definition of Modular Inverse: The modular inverse \(x\) exists if and only if \(a\) and \(m\) are coprime (their greatest common divisor, GCD, is 1).Extended Euclidean Algorithm: This algorithm is the standard, efficient way to find the inverse. It determines integers \(x\) and \(y\) that satisfy Bézout's identity: \(a\times x+m\times y=\text{gcd}(a,m)\). When \(\text{gcd}(a,m)=1\), the \(x\) value produced by the algorithm is the modular inverse.Algorithm Steps: The algorithm iteratively reduces the problem using the standard Euclidean algorithm steps, while simultaneously tracking the coefficients that satisfy Bézout's identity.
How Can It Help Others:
Enables Secure Cryptography: It is fundamental to public-key encryption algorithms like RSA, which secure sensitive data transmissions (e.g., banking details, private messages) by deriving the private decryption keys necessary to decode encrypted messages.
Verifies Data Integrity: The function is applied in standard error-checking systems, such as the generation and validation of check digits for ISBN and IBAN numbers, helping computers quickly detect input errors or data corruption.
Optimizes Computer Algorithms: In certain computational environments, the modular inverse allows division operations to be converted into faster multiplication operations, significantly speeding up algorithms used in digital signal processing and various mathematical computations. 

ques30)Write a function Carmichael Number Check is_carmichael(n) that checks if a composite number n satisfies aⁿ⁻¹ ≡ 1 mod n for all a coprime to n.
What We Did:
We created a Python function, is_carmichael(n), to determine if a given integer n is a Carmichael number. We also implemented helper functions is_prime(k) and get_prime_factors(n) to assist in this check. The main function uses Korselt's Criterion, a necessary and sufficient condition for a composite number to be a Carmichael number. 
What We Learned: We learned about Korselt's Criterion, a powerful mathematical theorem that simplifies the identification of Carmichael numbers. Instead of checking every integer a coprime to n (which is computationally expensive), we only need to verify two conditions based on n's prime factors: n must be square-free (not divisible by the square of any prime).For every prime factor p of n, the value p - 1 must evenly divide n - 1. The smallest Carmichael number is 561, which factors into \(3\times 11\times 17\). We verified that \(3-1=2\), \(11-1=10\), and \(17-1=16\) all divide \(561-1=560\). 
How Can It Help Others:
Primality Testing Education: This function illustrates a major limitation of the Fermat Primality Test. Carmichael numbers are "absolute pseudoprimes" because they pass the Fermat test for all valid bases a, making the basic Fermat test unreliable for proving primality.
Algorithmic Efficiency: The implementation of Korselt's criterion demonstrates an efficient approach to solving number-theoretic problems that would be intractable using the direct definition for large numbers.
Cryptography Insight: Understanding Carmichael numbers is important in the study of public-key cryptography (like RSA), where the ability to distinguish between prime and composite numbers is essential for security protocols.

ques31)Implement the probabilistic Miller-Rabin test is_prime_miller_rabin(n, k) with k rounds.
What We Did:
We implemented a probabilistic primality testing algorithm called the Miller-Rabin test in Python. The function is_prime_miller_rabin(n, k) takes a number n and a number of rounds k as input. It uses a helper function miller_rabin_test to run a single check using a randomly chosen base a. We also implemented an efficient power_with_modulo function (or utilized pow()) to handle the large exponentiations efficiently.
What We Learned: Probabilistic vs. Deterministic Tests: We learned the difference between deterministic primality tests (which are slow for very large numbers) and probabilistic tests (which are fast but have a tiny chance of error). The Miller-Rabin test guarantees that a "composite" result is correct, while a "prime" result means the number is a "strong probable prime" with a very low error probability (less than \((1/4)^{k}\)).Modular Exponentiation: The core efficiency of the algorithm relies on quickly computing \(a^{d}\quad (\mod n)\).Algorithm Logic: We learned how to decompose \(n-1\) into \(2^{s}\cdot d\) and check specific congruence conditions based on Fermat's Little Theorem and properties of square roots of unity modulo \(n\).Rabin's Optimization: By running the test multiple times (k rounds) with different random bases, the probability of a composite number passing all tests becomes astronomically small, making it reliable for practical applications.
How Can It Help Others:
Cryptography Applications: This is one of the most widely used algorithms for generating and verifying large prime numbers required in modern cryptography, such as RSA and Diffie-Hellman key exchange [1]. It ensures that the keys used to secure online communication are mathematically sound.
Efficient Prime Generation: Developers need fast ways to find primes with hundreds or thousands of digits. The Miller-Rabin test provides a robust and extremely fast method compared to trial division or deterministic methods like the AKS primality test [1].
Computer Science Education: It serves as an excellent case study in algorithms for probability, number theory, and how practical, fast, randomized algorithms can outperform slow, deterministic ones when a negligible error rate is acceptable.
