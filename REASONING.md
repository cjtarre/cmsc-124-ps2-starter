# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Implicit coercion promotes logical and integer values to double when a double is present. The result is a double vector of length 3 with no dimensions. 

## P02
Atomic vectors are coerced to the highest type present. Because a character value is included, all elements become character, giving length 3 with no dimensions.

## P03
Vector addition applies recycling to the shorter vector. The two-element integer vector is reused across four positions, producing an integer vector of length 4 with no dimensions. 

## P04
Positive integer indexing selects the specified positions in the given order and preserves their names. The result is an integer vector of length 2 with no dimensions. 

## P05
Negative indexing excludes the specified position while preserving the order of the remaining elements. The result is an integer vector of length 2 with no dimensions. 

## P06
Logical indexing retains elements where the condition is TRUE. 'is.na(x) | x > 10' selects the missing value and the value greater than 10, producing an integer vector of length 2 with no dimensions. 

## P07
A factor is stored internally as an integer vector with associated levels. It therefore has integer type, length 3, and no dimensions.

## P08
A list can contain elements of different types without coercion to a common atomic type. This list has two elements, so its type is list, its length is 2, and it has no dimensions.

## P09
A data frame is internally a list of equal-length columns with row and column dimensions. Its type is list, its length is 2, and its dimensions are 2x2.

## P10
Matrix addition recycles the shorter vector according to column-major storage order. The result remains integer, has length 6, and retains dimensions 2x3.

## P11
The 'mean()' function returns NA when missing values are present unless they are removed. The result is a double NA of length 1 with no dimensions

## P12
Setting 'na.rm = TRUE' removes missing values before computing the mean. The result is the double value 9 with length 1 and no dimensions.

## P13
Assigning a double value to an integer vector widens the entire vector to double. The vector retains length 3 and has no dimensions.

## P14
The 'ifelse()' function performs element-wise conditional replacement, replacing the missing value with 0 and doubling the others. Subassignment then caps values above 15, producing a double vector of length 4 with no dimensions. 

## P15
An array is an atomic vector with a dimension attribute. The values remain integer, giving length 8 and dimensions 2x2x2. 

## P16
Subsetting a vector with zero (0L) returns an empty integer vector with zero length and no dimensions.