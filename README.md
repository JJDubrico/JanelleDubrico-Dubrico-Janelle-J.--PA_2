# Dubrico_2ECE-A - PA #2 (V2)

# 1.) NORMALIZATION PROBLEM:

**In this problem, normalization means rescaling values so they have a common scale. For a 5x5 random array X, we are asked to subtract the average of all elements and then divide by the standard deviation, giving a new array Z where values reflect how many standard deviations away they are from the mean.**

    import numpy as np # Imports the NumPy Library
    
    X = np.random.random([5,5]) # Generates a random 5 x 5 ndarray
    
    y = X.mean() # Calculates the mean
    z = X.std() # Calculates the standard deviation
    
    X_normalized = (X - y) / z # Normalizes the array
    np.save('X_normalized.npy', X_normalized) # Saves the result to a .npy file    
    
    print("Original Array:\n", X) # Display the original arrays
    print("\nNormalized Array:\n", X_normalized) # Displays the normalized arrays


  # 2.) DIVISIBLE BY 3 PROBLEM:

**We form a 10x10 array containing the squares of the numbers 1 through 100 in row-major order. Then we filter this array to keep only the elements divisible by 3 and save that result to div_by_3.npy.**

    import numpy as np # Imports the NumPy Library

    d = np.array([i**2 for i in range(1, 101)]).reshape(10, 10) # Creates an array of the squares of the first 100 positive integers

    divisible_by_3 = d[d % 3 == 0].reshape(3,11) # Identifies elements that are divisible by 3
    
    np.save('div_by_3.npy', divisible_by_3) # Saves the result to a .npy file
    
    print("Squares Array:\n", squares) # Displays the squares array
    print("Elements Divisible by 3:\n", divisible_by_3) # Displays the elements that are divisible by 3
    
--VERSION 2--
