# Data-Eng.-Project

I have created this data engineering project with the help of tools like AWS S3, snowflake and Power BI.
First divided the data in the chunk then uploaded to AWS. Then i have transferred it to the snowflake. Then I have queried the data. Finally, i have transferred it to Power BI for dashboard.

python to divide data into 5 chuks
import json

input_file  = "C:/Users/ADM/Desktop/RBc.csv"
output_folder = r"C:/Users/ADM/Desktop"

output_prefix = "split_file"

num_file  = 5

with open(input_file, "r", encoding = "utf-8") as f:
    total_lines = sum(1 for line in f)

total_lines 

lines_per_file = total_lines // num_file

lines_per_file

with open(input_file, "r", encoding = "utf-8") as f:
    for i in range(num_file):
        output_filename = f"{output_prefix}{i+1}.csv
        with open(output_folder, "w", encoding = "utf8") as 

with open(input_file, "r", encoding="utf-8") as f:  # Keep input file open
    for i in range(num_file):
        output_filename = f"{output_prefix}{i+1}.json"
        with open(output_folder, "w", encoding="utf8") as out_file:
            for j in range(lines_per_file):
                line = f.readline()  
                if not line:
                    break  # Stop if file ends early
                out_file.write(line)  # Write to output file




                
