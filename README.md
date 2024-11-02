# Dataset Preparation Guide

## Preparation Steps

1. **Combine Original Files**  
   Merge the four original files into a single dataset.

2. **Filter Malicious Traffic**  
   Select only the rows corresponding to malicious traffic for focused analysis.

3. **Group Attacks by Destination IP**  
   Organize the data by grouping attacks based on the destination IP address to identify attack patterns per target.

4. **Assign Attack IDs**  
   Create unique `attack_id`s for each attack instance based on defined threshold values.

5. **Generate Remaining Time Feature**  
   Calculate a `remaining_time` feature for each attack based on the attack’s total duration and cumulative attack duration. This processed file is saved as `Victim_Dataset/combined_dataset_sorted_remaining_time.csv`.

6. **Create Data Sequences and Split Dataset**  
   Construct sequences of 30 flows for each `attack_id`, then split the data into train, validation, and test sets. The final dataset is saved in `final_seq_data`.

