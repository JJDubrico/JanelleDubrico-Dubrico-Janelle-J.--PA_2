# Dubrico_ECE2112 [PA #2]

# 1.) NORMALIZATION PROBLEM:

    Using the import convention:
    import numpy as np # Used to access the NumPy library
    
    X = np.random.random([5,5]) # Generate a random 5 x 5 ndarray
    
    y = X.mean()
    z = X.std() # Calculate the mean and standard deviation
    
    X_normalized = (X - y) / z # Normalize the array
    np.save('X_normalized.npy', X_normalized) # Save the result to a .npy file    
    
    print("Original Array:\n", X)
    print("\nNormalized Array:\n", X_normalized) # Display the original and normalized arrays


  # 2.) DIVISIBLE BY 3 PROBLEM:

    Using the import convention:
    import numpy as np # Used to access the NumPy library

    d = np.array([i**2 for i in range(1, 101)]).reshape(10, 10) # Create an array of the squares of the first 100 positive integers

    divisible_by_3 = d[d % 3 == 0].reshape(3,11) # Identify elements that are divisible by 3
    
    np.save('div_by_3.npy', divisible_by_3) # Save the result to a .npy file
    
    print("Squares Array:\n", squares)
    print("Elements Divisible by 3:\n", divisible_by_3) # Output the results for verification
    
