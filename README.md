# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
import math

p = [0.55,0.15,0.15,0.1,0.05]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,3,3,3,3]
n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency
eff = round(hs / L, 3)

# Redundancy
red = round(1 - eff, 3)

# Variance
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

# Output
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

# Calculation:
![WhatsApp Image 2025-09-19 at 11 42 53_ea684a22](https://github.com/user-attachments/assets/7b5cf9a8-dd7a-4b41-8877-8fb448e82b34)

![WhatsApp Image 2025-09-19 at 11 42 53_e642665e](https://github.com/user-attachments/assets/b3a07147-1930-4302-8f21-8e2d10cff9f4)

# Output
<img width="692" height="742" alt="image" src="https://github.com/user-attachments/assets/bc93f4a6-19e0-41c7-bd31-28135fc74ff9" />
<img width="353" height="180" alt="image" src="https://github.com/user-attachments/assets/7c9ee88b-a0e4-44fe-990e-9d6ef54767ea" />

# Results:
Thus the discrete memoryless source with symbols and statistics {0.55,0.15,0.15,0.1,0.05} for its output was successfully calculated. 
