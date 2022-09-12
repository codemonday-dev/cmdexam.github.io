## Case 3: Data integrity

Existing Component: Source system export CSV data to the storage. We are building system to bring in this data on the daily basis e.g., every day 9 o'clock.

Process:
1. Source system export all information on the source table as CSV.
2. Our system bring in the data
3. Our system expose this data as an API

Task: Please design the solution to ensure data correctness and integrity in a timely manner.