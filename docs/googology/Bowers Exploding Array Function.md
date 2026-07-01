# Bowers' Exploding Array Function
**Bowers' Exploding Array Function** (**BEAF** for short) is a notation, like Knuth's Up Arrows and Conway's Chained Arrows, but way, WAY more powerful. <br>
<br>
**PLEASE KEEP IN MIND THAT THERE IS NO AGREED UPON DEFINITION FOR SOME OF THE MORE COMPLICATED PARTS OF BEAF NOTATION**


## Operator Notation
Operator Notation is the simplest form of BEAF and provides the foundation for the entire.
The basis of this notation is defined like this:

$$a\\{n\\}b = a \uparrow ^{n} b$$ <br>
$$\therefore \left\\{\begin{array}{ll} a\\{1\\}b = a^{b} \\\ a \\{n\\}b = \underbrace{a\\{n - 1\\}a\\{n - 1\\}...\\{n - 1\\}a\\{n - 1\\}a}_ \text{b times} \end{array} \right.$$

Essentially, a array n b is equal to a with the nth hyperoperator of b.
However, we can nest arrays in arrays to make it even more insane.

$$a\\{\\{n\\}\\}b = \underbrace{a\\{a\\{... a\\{a}_ \text{expanded b times}\\} a ...\\}a\\}a \hspace{0.5cm} \text{if } n = 1$$
$$a\\{\\{n\\}\\}b = \underbrace{a\\{\\{n - 1\\}\\}a\\{\\{n - 1\\}\\}...\\{\\{n - 1\\}\\}a\\{\\{n - 1\\}\\}a}_ \text{b times} \hspace{0.5cm} \text{if } n > 1$$

Here, a double array n b is defined as b layers of arrays with a on each side, provided that n is 1. In other words, this is expanding an array of a b times over itself.
When n is greater than one, instead of nesting them, we expand them out, decreasing the number inside of the braces by one in the expansion. Arrays with numbers of brackets more than two are defined in the same way. <br>

You may have noticed that these brackets take up a fair bit of space. This is a problem, especially when dealing with big nested arrays. Luckily, there is a shorthand method for BEAF operator notation.

$$\underbrace{a\\{...\\{a\\}...\\}b}_ \text{k enclosed brackets} = a\\{n\\}^{k}a$$

This shorthand notation is about as powerful as Conway's Chained Arrows, and we haven't even scratched the surface!

## Linear Notation
Operator Notation is starting to burst at the seams, so let us introduce Linear Notation. <br>
The basis for BEAF Linear Notation is defined as:

$$\\{a, b, c, d\\} = a\\{c\\}^{d}b$$
$$\therefore \left\\{\begin{array}{ll} \\{a, b, 1, 1\\} = a^{b} \\\ \\{a, b, 1, d\\} = \underbrace{\\{a, a\\{a, a,...\\{a, a, d - 1\\}..., d - 1\\}, d - 1\\}}_ b \hspace{0.5cm} \text{if } d > 1 \\\ \\{a, b, c, d\\} = \underbrace{\\{a,\\{a,...\\{a, a, c - 1, d\\}..., c - 1, d\\}, c - 1, d\\}}_ b \hspace{0.5cm} \text{if } c > 1 \end{array} \right.$$

Ones are considered defaults, so we can chop off the end of the array if it only contains ones. <br>
This way, rule 1 can be simplified like this:

$$\\{a, b\\} = a^{b}$$

Rules two and three can also be somewhat simplified by relying on their recursive nature.

$$\\{a, b, 1, d\\} = \underbrace{\\{a, a\\{a, a,...\\{a, a, d - 1\\}..., d - 1\\}, d - 1\\}}_ b$$
