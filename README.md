#!/bin/bash

input_file="a1.txt"
output_file="a1_modified.txt"

while IFS= read -r line; do
    if [[ $line =~ [^a-zA-Z\ ] ]]; then
        echo "$line" >> "$output_file"
    else
        modified_line=$(echo "$line" | sed 's/\bsanket\b/hcl/g')
        echo "$modified_line" >> "$output_file"
    fi
done < "$input_file"

echo "Processing complete. Modified lines are saved in $output_file"
