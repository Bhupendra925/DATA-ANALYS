# DATA-ANALYS
import pandas as pd
import matplotlib.pyplot as plt

# Load the uploaded file
df = pd.read_csv(r"C:\Users\bhupe\Downloads\students.csv")

print("Preview of data:")
print(df.head())

# Calculate average
df["Average"] = df[["Math", "Science", "English"]].mean(axis=1)
print("\nAverage marks:")
print(df[["Name", "Average"]])

# Plot
plt.figure(figsize=(8, 5))
plt.bar(df["Name"], df["Average"], color="yellow")
plt.title("Average Marks of Students")
plt.xlabel("Student Name")
plt.ylabel("Average Marks")
plt.grid(True)
plt.tight_layout()
plt.show()
