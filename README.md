## MultiThreading Assignment

This Python script demonstrates matrix multiplication with multithreading. It calculates the product of 100 random matrices of size 1000x1000 with a constant matrix of the same size using multiple threads. It also measures the time taken and CPU usage for different numbers of threads.

### Prerequisites
Before running the script, ensure you have the following installed:
- Python 3.x
- NumPy
- psutil (install using pip install psutil)
- Matplotlib

### Methodology

#### Matrix Multiplication Implementation:
1. Random matrices of size 1000x1000 are generated using NumPy.
2. A constant matrix of the same size is used for multiplication.
3. Matrix multiplication is performed using multiple threads, with the number of threads varying from 1 to a specified maximum.
4. Time taken for matrix multiplication is measured using Python's time module.

#### CPU Usage Monitoring:
- CPU usage is monitored using the psutil library, which provides an interface for retrieving CPU utilization statistics.
- CPU usage for each CPU core is measured during matrix multiplication with different numbers of threads.

### Experimental Procedure
1. Initialize the experiment by importing necessary libraries and defining constants such as matrix size and maximum number of threads.
2. Generate random matrices and define the constant matrix for multiplication.
3. Perform matrix multiplication using a single thread and measure the time taken as the baseline.
4. Iterate over different numbers of threads, ranging from 1 to the maximum specified.
   - For each number of threads:
     - Create a pool of threads using Python's threading module.
     - Distribute the matrix multiplication tasks among the threads.
     - Measure the time taken for matrix multiplication and record CPU usage statistics.
5. Plot the results:
   - Time Taken vs Number of Threads graph to visualize the impact of multithreading on execution time.
   - Compare the actual time taken with the expected time based on the number of threads.

### Results
The script generates two graphs:
- Time Taken vs Number of Threads: This graph shows the time taken for matrix multiplication using different numbers of threads. It also compares the actual time taken with the expected time.
- CPU Usage vs Number of Threads: This graph shows the CPU usage for each CPU core as green grid lines. The peak points are labeled as CPU 0, CPU 1, CPU 2, and so on.
  ### Time Taken (s) vs Threads

| Threads | Time Taken (s) |
|---------|----------------|
| 1       | 18.023243      |
| 2       | 17.352902      |
| 3       | 16.807090      |
| 4       | 17.607774      |
| 5       | 17.891347      |
| 6       | 16.900062      |
| 7       | 15.803305      |
| 8       | 15.763509      |


### Conclusion
From the results obtained, we can draw the following conclusions:
- As the number of threads increases, the time taken for matrix multiplication generally decreases, up to a certain point. Beyond that point, the overhead of thread creation and management may outweigh the benefits of parallelism.
- CPU usage increases as the number of threads increases, as expected. However, it's essential to note that the distribution of CPU usage across cores may vary depending on the system architecture and workload.
- It's crucial to optimize the number of threads based on the specific hardware configuration and workload characteristics to achieve the best performance.
- This experiment demonstrates the potential benefits of multithreading for computationally intensive tasks such as matrix multiplication, especially on multicore systems.
