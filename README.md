# Code below the screenshot
![731123480384c41746f1283b454164d](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/a73e8b5b-47fd-4dce-9b3c-053eb2a29630)
![bad43a5adff8a9f20553aaaf03a1e93](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/94442253-5fe9-4057-a941-4b880a58cac6)
![fffd959e51eb98f1da44dca27df6bcc](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/7ae11150-546e-438e-be5c-7ad73af47574)
![9f80bbd5817bc4e46dd4a550581f1b3](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/31f4c83f-82b6-4a2d-a812-1b6aaa7e98c4)
![7d663f1dbb38fe3be0a446ce66f013e](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/de0ed032-c8da-44ce-afc8-b3676346e7df)
![e923c9ff38bda09ffb1cce4906a3b88](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/b51c56b6-816e-4312-b08a-2330dbe21148)
![8934e9bc75035323b2b752965f1313b](https://github.com/MENGZZZZZZZ/CSC245-HW1/assets/161723991/4a76cd51-8e46-4215-82f0-2186d6508738)



import numpy as np
# Create a rank 2 (2D) array
my_array = np.array([[11, 12, 13, 14], [15, 16, 17, 18]])
print(my_array)


# 1. Create an array with 4 rows and 3 columns of zeros. Your results should look as below:
array_zeros = np.zeros((4, 3))
print(array_zeros)


# 2. Create an array of ones that has 3 rows and 4 columns. 
array_ones = np.ones((3, 4))
print(array_ones)


# 3. Create an array containing integers 4 to 13 inclusive. Your results should look as below:
array_integers = np.arange(4, 14)
print(array_integers)


# 4. Create an array containing
array_floats = np.arange(0, 6, 1.5)
print(array_floats)


# 5. Create a 2 by 2 array containing '4' in each position. Your results should look like this
array_fours = np.full((2, 2), 4)
print(array_fours)


# 6. Create 2 matrices
identity_matrix = np.eye(4)
print(identity_matrix)

diagonal_matrix = np.diag([10, 12])
print(diagonal_matrix)


# 7. Create a 3 by 3 array with random floats in [0, 10].
array_random_floats = np.random.uniform(0, 10, (3, 3))
print(array_random_floats)


# 8. Create a 3 by 3 array with random integers in [10, 20]. 
array_random_integers = np.random.randint(10, 21, (3, 3))
print(array_random_integers)



# 1. Use this array for the following practice: myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])
# a. Get a subarray of the first row and first 2 columns
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
subarray_a = myArray[0, :2]
print(subarray_a)
# b. Change all elements in 1st and second row to 0
myArray[:2] = 0
print(myArray)


# Create an array that contains [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20] and reverse the order.
reversed_array = np.arange(21)[::-1]
print(reversed_array)


# Reshaping
myArray = np.array([[11, 12, 13], [14, 15, 16]])
reshaped_array = myArray.reshape(3, 2)
print(reshaped_array)


# MATH
myArray = np.arange(10)
# 1
squared_array = np.square(myArray)
print(squared_array)
# 2
sqrt_array = np.sqrt(myArray)
print(sqrt_array)
# 3
result_array = squared_array * sqrt_array
print(result_array)


# ADDING ELEMENTS
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
# 1
new_row = np.array([[20, 21, 22]])
myArray = np.vstack((myArray, new_row))
print(myArray)
# 2
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
new_column = np.array([[30], [40], [50]])
myArray = np.hstack((myArray, new_column))
print(myArray)


# INSERTING ELEMENTS
# 1. Add 1 column of 1 to this array: myArray = np.zeros((2, 2))
myArray = np.zeros((2, 2))
new_column = np.ones((2, 1))
myArray = np.hstack((myArray, new_column))
print(myArray)


# 2. Add 2 rows of 2 to the answer from part 1
new_rows = np.full((2, myArray.shape[1]), 2)
myArray = np.vstack((myArray, new_rows))
print(myArray)


# 3. Remove the last column
myArray = np.delete(myArray, -1, axis=1)
print(myArray)


# 4. Remove the last row
myArray = np.delete(myArray, -1, axis=0)
print(myArray)


# DELETING ELEMENTS
myArray = np.matrix([[1, 2, 3], [4, 5, 6], [9, 8, 7]])
myArray = np.delete(myArray, 1, axis=1)
print(myArray)


# TEST EXERCISE
exercise_1 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
exercise_1[exercise_1 % 2 == 1] = -1
print(exercise_1)


exercise_2 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8])
exercise_2 = exercise_2.reshape(3, -1)
print(exercise_2)


exercise_3 = np.arange(4).reshape(2, -1) + 202
print(exercise_3)


# Generate a 1-D array of 10 random integers between 30 and 40 (inclusive)
random_array = np.random.randint(30, 41, size=10)
print(random_array)

# Find the positions of:elements in x where its value is more than its corresponding element in y, and elements in x where its value is equals to its corresponding element in y.
x = np.array([21, 64, 86, 22, 74, 55, 81, 79, 90, 89])
y = np.array([21, 7, 3, 45, 10, 29, 55, 4, 37, 18])
positions_more = np.where(x > y)
positions_equal = np.where(x == y)
print(positions_more, positions_equal)


# Extract the first four columns of this 2-D array
exercise_6 = np.arange(100).reshape(5, -1)
first_four_columns = exercise_6[:, :4]
print(first_four_columns)



