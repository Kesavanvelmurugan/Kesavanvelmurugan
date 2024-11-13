import pandas as pd

# Sample data: Agricultural raw materials with categories and HS codes
data = [
    {"Material": "Wheat", "Category": "Grain", "HS_Code": "1001"},
    {"Material": "Maize (Corn)", "Category": "Grain", "HS_Code": "1005"},
    {"Material": "Rice", "Category": "Grain", "HS_Code": "1006"},
    {"Material": "Soybeans", "Category": "Oilseed", "HS_Code": "1201"},
    {"Material": "Cotton", "Category": "Fiber", "HS_Code": "5201"},
    {"Material": "Palm Oil", "Category": "Oil", "HS_Code": "1511"},
]

# Create a DataFrame for better data handling
df = pd.DataFrame(data)

# Display the DataFrame
print("Agricultural Raw Materials Data:")
print(df)

# Filtering examples
# 1. Filter materials by category
grains = df[df["Category"] == "Grain"]
print("\nGrain Category Materials:")
print(grains)

# 2. Find materials with a specific HS code
specific_hs_code = df[df["HS_Code"] == "1005"]
print("\nMaterials with HS Code 1005:")
print(specific_hs_code)

# Save the data to a CSV file
df.to_csv("agricultural_raw_materials.csv", index=False)
print("\nData has been saved to 'agricultural_raw_materials.csv'.")
