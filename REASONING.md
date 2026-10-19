# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Atomic vectors use a common type. Because a double is present, the logical and integer values are coerced to double, while the vector keeps length 3 and has no dimensions.

## P02
Atomic vectors use a common type. Because a character value is present, the integer and logical values are coerced to character, producing a length-3 vector with no dimensions.

## P03
R recycles the shorter vector during vectorized arithmetic. The two-element integer vector is reused across the four elements, so the result remains integer, has length 4, and has no dimensions.

## P04
Positive indexing selects elements in the order given by the index and preserves their names. Two integer elements are selected, so the result has length 2 and no dimensions.

## P05
Negative indexing removes the positions named by the index. Removing the second element leaves two integers, so the result has length 2 and no dimensions.

## P06
Logical indexing keeps elements where the condition is TRUE. The condition selects the missing value and the value greater than 10, producing an integer vector of length 2 with no dimensions.

## P07
A factor is stored internally as an integer vector with levels kept as an attribute. It therefore has integer type, length 3, and no dimensions.

## P08
A list can contain elements of different types without coercing them to one atomic type. This list has two named elements, so its type is list, its length is 2, and it has no dimensions.

## P09
A data frame is internally a list of equal-length columns and also has row and column dimensions. With two columns and two rows, its type is list, its length is 2, and its dimensions are 2 by 2.

## P10
R performs matrix arithmetic element by element and recycles the shorter vector through the matrix in column-major order. The result remains integer, contains 6 elements, and keeps the matrix dimensions of 2 by 3.

## P11
By default, mean() does not remove missing values. Because the vector contains NA, the result is a double NA of length 1 with no dimensions.

## P12
Setting na.rm = TRUE removes missing values before computing the mean. The remaining values average to 9, returned as a double scalar of length 1 with no dimensions.

## P13
Assigning a double value into an integer vector causes the whole atomic vector to be coerced to double. The vector still has three elements and no dimensions.

## P14
ifelse() works element by element, replacing the missing score with 0 and doubling the others. The later indexed assignment caps values above 15, leaving a double vector of length 4 with no dimensions.

## P15
An array stores one atomic vector together with a dimension attribute. The integers 1 through 8 remain integer, giving length 8 and dimensions 2 by 2 by 2.

## P16
Index 0 selects no elements in R. The result is therefore an empty integer vector with length 