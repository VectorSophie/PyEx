import random

def generate_dataset(factor1_name, factor1_range, factor2_name, factor2_range, dataset_size, decimal_places):
    # Unpack factor ranges
    f1_min, f1_max = factor1_range
    f2_min, f2_max = factor2_range
    
    dataset = []
    
    for _ in range(dataset_size):
        # Generate random values within the specified ranges and round to decimal_places
        f1_value = round(random.uniform(f1_min, f1_max), decimal_places)
        f2_value = round(random.uniform(f2_min, f2_max), decimal_places)
        
        # Append to dataset
        dataset.append({factor1_name: f1_value, factor2_name: f2_value})
    
    return dataset

# Get inputs from user
factor1_name = input("Enter the name of Factor 1: ")
factor1_min = float(input(f"Enter the minimum value for {factor1_name}: "))
factor1_max = float(input(f"Enter the maximum value for {factor1_name}: "))
factor1_range = (factor1_min, factor1_max)

factor2_name = input("Enter the name of Factor 2: ")
factor2_min = float(input(f"Enter the minimum value for {factor2_name}: "))
factor2_max = float(input(f"Enter the maximum value for {factor2_name}: "))
factor2_range = (factor2_min, factor2_max)

dataset_size = int(input("Enter the number of data points to generate: "))
decimal_places = 0

random.seed(69)  # For reproducibility

generated_dataset = generate_dataset(factor1_name, factor1_range, factor2_name, factor2_range, dataset_size, decimal_places)

# Print the generated dataset
for data_point in generated_dataset:
    print(data_point)
