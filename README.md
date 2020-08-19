# Scalable Data Analysis in Python with DASK

This repo includes course and labs work related to [Dask](https://dask.org/)
The course is: [scalable-data-analysis-in-python-with-dask/](https://www.udemy.com/course/scalable-data-analysis-in-python-with-dask/)

The code will be in python 3.X

#### What is DASK
[Dask](https://dask.org/) is a library in Python, that allows users to:
- parallelize their existing code in python
- Scale out their existing code over clusters

It even has support for task scheduling and it can easily be used with libraries like NumPy, Pandas...
It offers a familiar API for parallel/distributed computing.

##### Use Cases for DASK:
- parallelize python code without major change
- load large datasets (bigger than size of RAM) and perform computation using specialized DASK structures like Dask arrays, Dask Dataframes,...
- scale out our code from single machine to large clusters
- support for task scheduling for complex applications

##### Features of DASK:
- allows parallelizing existing Python code w/o doing many changes
- has specialized data structures which allows users to load data larger than the size of memory (RAM) like:
 - Dask arrays
 - Dask Dataframes
 - Dask Bags
- has specialized blocked algorithms, which can perform different types of computations on chunks of datasets
- perform large computations with less memory footprint
- allows you to scale you code easily to a cluster of notes:
 - has provisions for handling nodes failures
 - can easily add notes on the fly
- Familiar Python API (similar to NumPy and Pandas) => minimum overhead to make our code compatible with DASK
- has provision for task-scheduling (similar to Apache AirFlow)e
- real-time responsive dashboard to view the status of jobs
- static profiler installed on each node for performance Analysis

##### Limitations of Dask
- In a distributed setting, the workers have the same limitations of Python processes.
- Assigning of tasks to workers may not always be optimal
- it makes the assumption that you data and functions are both serializable
- in case of failures, Dask may rerun your code multiple times
- any side effects based on your code, should be idempotent in nature (multiple identical requests/executions has the same effect as making a single request/execution)

##### Setting up DASK
To install locally using pip/conda:
`pip install dask`

To install all components of dask (like dask arrays), run:
``pip install dask[complete]`

You can then check running:
```
python
>>> import dask
>>>
```
