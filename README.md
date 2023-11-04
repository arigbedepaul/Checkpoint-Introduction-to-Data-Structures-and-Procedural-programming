# Checkpoint-Introduction-to-Data-Structures-and-Procedural-programming

Rephrased:

---

# Introduction to Data Structures and Procedural Programming - Checkpoint

## Problem 1: Algorithm to Calculate the Sum of Distinct Elements from Sets

In this problem, we aim to develop an algorithm to find the sum of all distinct elements from two sets. Given two arrays, ArraySet1 and ArraySet2, we want to calculate the sum of elements that are unique to either of these sets.

# **Algorithm:**

- We have two sets, ArraySet1 and ArraySet2.
- We use the variables i, j, and k for iteration.
- A variable called Sum is initialized to store the sum of distinct elements.

# **Processing ArraySet1:**

- We iterate through the elements of ArraySet1 using the index variable i.
- To identify distinct elements, we initialize a variable called "distinct" to TRUE.
- With the help of a nested loop, we iterate through the elements of ArraySet2 using the index variable j. We check if the element at index i in ArraySet1 is equal to the element at index j in ArraySet2. If they match, we set "distinct" to FALSE, indicating that it's not a distinct element.
- If the element at index i in ArraySet1 is distinct, we add it to the sum.

# **Processing ArraySet2:**

- Similarly, we iterate through the elements of ArraySet2 using the index variable k.
- We initialize a new "distinct" variable to TRUE.
- Within a nested loop, we iterate through the elements of ArraySet1 using the index variable j.
- We check if the element at index k in ArraySet2 is equal to the element at index j in ArraySet1. If they match, the "distinct" variable is set to FALSE, indicating that it's not a distinct element.
- If the element at index k in ArraySet2 is distinct, we add it to the sum.

# **Final Step:**

- Finally, the algorithm prints the value of the sum, which represents the sum of distinct elements from both arrays.

**Practical Demonstration:**

- Let ArraySet1 be an array: [3, 1, 7, 9]
- Let ArraySet2 be an array: [2, 4, 1, 9, 3]

The algorithm iterates through ArraySet1 and checks each element for its presence in ArraySet2. If an element is found in both arrays, it is not added to the sum.

- For ArraySet1[0] (value 3), it is found in ArraySet2 (at index 4), so it's not added to the sum.
- For ArraySet1[1] (value 1), it is found in ArraySet2 (at index 2), so it's not added to the sum.
- For ArraySet1[2] (value 7), it is not found in ArraySet2, so it's added to the sum.
- For ArraySet1[3] (value 9), it is found in ArraySet2 (at index 3), so it's not added to the sum.

Similarly, the algorithm checks ArraySet2 for elements not present in ArraySet1.

- For ArraySet2[0] (value 2), it is not found in ArraySet1, so it's added to the sum.
- For ArraySet2[1] (value 4), it is not found in ArraySet1, so it's added to the sum.
- For ArraySet2[2] (value 1), it is found in ArraySet1 (at index 1), so it's not added to the sum.
- For ArraySet2[3] (value 9), it is found in ArraySet1 (at index 3), so it's not added to the sum.
- For ArraySet2[4] (value 3), it is found in ArraySet1 (at index 0), so it's not added to the sum.

Sum all the elements added to the sum in the previous steps:

7 (ArraySet1[2]) + 2 (ArraySet2[0]) + 4 (ArraySet2[1]) = 13

The final value of "sum" is 13.

## Problem 2: Algorithm to Determine Orthogonality of Vectors

In this problem, we'll develop an algorithm to determine whether pairs of real-valued vectors are orthogonal. Orthogonal vectors have a dot product equal to zero.

**Explanation of the Procedure (dot_product):**

The algorithm uses a procedure called dot_product to calculate the dot (scalar) product of two vectors, v1 and v2, where v1 and v2 are vectors of real numbers. For any n pairs of vectors, the algorithm determines whether the two vectors are orthogonal by calling this procedure.

**Procedure Explanation:**

- The procedure `dot_product(v1, v2: ARRAY_OF REAL; VAR ps: REAL; n: INTEGER)` calculates the dot product of two vectors, v1 and v2.
- It takes the following parameters:
  - v1: An array representing the first vector.
  - v2: An array representing the second vector.
  - ps: A variable that will store the result of the dot product.
  - n: The dimension of the vectors, indicating how many elements are in each vector.

**Steps within the dot_product Procedure:**

1. Initializes the variable ps to 0

, which will accumulate the dot product.
2. The procedure enters a loop that iterates from 0 to n - 1, considering the dimension of the vectors.
3. Inside the loop, it calculates the dot product by taking the element at the same index from v1 and v2, multiplying them, and adding the result to ps.
4. The loop continues until it has processed all elements of the vectors.

**Example:**

Suppose we have two vectors of dimension 3:
- Vector v1: [2, 3, 4]
- Vector v2: [1, 5, 2]

We want to calculate the dot product of these two vectors using the dot_product procedure.

- v1 and v2 are passed as the v1 and v2 parameters to the procedure.
- The dimension is n = 3.

Here's the calculation within the dot_product procedure:

- Initialize ps to 0.
- Loop through elements:
  - For i = 0, we have ps = 0 + (2 * 1) = 2
  - For i = 1, we have ps = 2 + (3 * 5) = 17
  - For i = 2, we have ps = 17 + (4 * 2) = 25

The final result is ps = 25, which is the dot product of the two vectors v1 and v2. In this case, the dot product is not zero, so these vectors are not orthogonal.

**Algorithm (Orthogonality Check):**

- In addition to variables already stated above, we define i, j, k as integer variables used for iterating through vector pairs.
- The algorithm starts by requesting the user to input the dimension of the vectors, which is the number of elements in each vector.
- Dimension Validation: It ensures that the entered dimension is within a valid range using an IF-THEN-ELSE statement. For instance, the code checks that n is between 1 and 50. This process ensures that the dimension is within a reasonable and practical value.
- If the vectors' dimension is valid, the algorithm enters a loop that runs for n iterations, where n is the dimension entered by the user.
- Inside the loop, the algorithm reads the elements of both v1 and v2 using nested loops. It reads n elements for each vector.
- After reading the elements of v1 and v2, the algorithm calls the dot_product procedure to calculate the dot product of the two vectors (v1 and v2), passing the vectors, 'n', and 'ps' variable as parameters.
- Thereafter, the algorithm checks if the dot product (ps) is equal to 0.
- If ps is equal to 0, it implies the vectors are orthogonal, and it prints "Vectors are orthogonal."
- If ps is not equal to 0, it implies the vectors are not orthogonal, and it prints "Vectors are not orthogonal."

This algorithm is designed to process multiple pairs of vectors with the user-specified dimension and determine whether each pair is orthogonal based on the dot product.

---

Please note that the rephrased content maintains the original content's structure and explanations but is presented in a clearer and more concise manner.
