# Google-Girl-Hackathon
# Setting up the environment
The notebook "Google_Girl_Hackathon.ipynb" can be downloaded and be run on Google Colab. First the notebook needs to be downloaded along with the data file "data.xlsx". 
Steps:
1. Download both the files "Google_Girl_Hackathon.ipynb" and "data.xlsx"
   
3. Go to Google Colab and upload the downloaded notebook "Google_Girl_Hackathon.ipynb".
   Upload->Browse-> select "Google_Girl_Hackathon.ipynb"
   
5. Once the uploading is completed, upload the data file.
   Under 'Files' ribbon->'Upload to session storage'->'data.xlsx'->open->ignore the warning if any
   
Once the data is uploaded, the code is ready to be run. There are two code blocks. Both can be run using:
Runtime->Run all

# Details on the data
The trace table used in this code is a demo dataset generated with the help of some AI tools and with some manual alterations. This data mimics the simulator data and has been generated only to test the latency and bandwidth calculation code. In order to implement the RL algorithm in the second part of the problem statement, we will require the actual simulator data with more data points.

# Formulas used for latency and bandwidth calculation
average latency for a read operation = total time taken to serve all the read operations / number of read operations

average latency for a write operation = total time taken to serve all the write operations / number of write operations

total latency = total time taken for all reads and writes

average latency for any operation = total latency /total number of reads and writes

total data transferred = total number of reads and writes * 32

bandwidth = total data transferred / total latency

# Approach
Latency for each read operation is calculated from the trace table. But there is no similar logic given for calculaion of write latencies, so I have considered a constant write latency for all the write operations.

# Complexity Analysis
Time complexity: O(N) where N=number of rows in the trace table

Space complexity: O(M) where M=number of unique data addresses being accessed via read and write operations from both IO and CPU units
