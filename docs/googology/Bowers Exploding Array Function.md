# Bower's Exploding Array Function
**Bower's Exploding Array Function** (**BEAF** for short) is a notation, like Knuth's Up Arrows and Conway's Chained Arrows, but way, WAY more powerful.

The basis of the notation is defined like this:

$a\\{n\\}b = a \uparrow ^{n} b$ <br>
$a\\{\\{n\\}\\}b = \underbrace{a\\{a\\{...\\{a\\}...\\}a\\}a}_ \text{n times} \hspace{0.5cm} \text{if n = 1}$ <br>
$a\\{\\{n\\}\\}b = \underbrace{a\\{\\{n - 1\\}\\}a ... a\\{\\{n - 1\\}\\}a}_\text{n times} \hspace{0.5cm} \text {if n > 1}$ 
