# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Implicit coercion rules promotes logical and integer elements to double when mixed with a double in a vector. Double is in a higher order than integer.

## P02
Combining numeric, character, and logical values in a single vector forces all elements to be coerced to character type since it is the highest order.

## P03
Vector addition applies recycling rules, adding the shorter vector elements to the longer vector.

## P04
Positive integer indexing selects elements at those specific positions while preserving names.

## P05
Negative indexing excludes the element at the specified position while retaining the remaining elements in their original order.

## P06
Logical indexing keeps elements where the condition evaluates to TRUE. 'is.na()' identifies missing values, and '|' combines the conditions.

## P07
The factor function creates a categorical variable stored internally as an integer vector with associated levels.

## P08
A list is a generic vector that can hold components of mixed data types and structures.

## P09
A data frame is structured as a list of equal-length vectors representing columns, with a two-dimensional row and column dimension.

## P10
Matrix addition recycles the shorter vector to match the matrix's elements in column-major order, preserving the matrix dimensions.

## P11
The mean function returns NA by default when missing values are present and na.rm = TRUE is not specified.

## P12
Setting na.rm = TRUE removes missing values before computing for the mean.

## P13
Assigning a double value into an integer vector element promotes the entire vector's storage type to double.

## P14
The ifelse function handles conditional replacement including missing values, followed by upper-bound clamping (n > 15) via vector assignment.

## P15
The array function organizes a sequential vector into a multi-dimensional structure specified by the dim parameter.

## P16
Subsetting a vector with zero (0L) returns an empty vector of the same type and zero length.