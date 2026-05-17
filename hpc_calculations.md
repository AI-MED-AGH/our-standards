# High-Performance Computing

## Introduction
---
High-Performance Computing (HPC) is a technology that uses clusters of powerful processors that work in parallel to process massive, multidimensional data sets and solve complex problems at extremely high speeds. Many providers gives also access to GPUs clusters.

In this article, we will discuss performing calculations using high-performance computers managed via queuing systems.

> [!INFO] While using Large infrastructures always remember to familiarize yourself with the guidelines and documentation.


## Cyfronet AGH
---
As a research society at AGH, we run scientific calculations on the infrastructure of the [Academic Computer Centre Cyfronet AGH](https://www.cyfronet.pl/en), which is equipped with high-quality hardware offering high computing power.

![[Pasted image 20260401221543.png]]

### How to get access as scientific club member?
- be an active member of the projects, as we use this infrastructure exclusively for scientific purposes, except in cases previously agreed with the provider.
- contact the person responsible for managing the calculations within our group (ask your Project Menager)


## Data transfer and storage
---
Transferring data to remote storage should be done always with safe protocols as sftp. You should not send a large number of small files. For this reason, you should compress the data before sending it. If the file size limit is exceeded, you should consider splitting the data set into smaller chunks.

Although a secure environment is provided, medical data must be anonymized; sensitive data should not be sent even to a secure environment.

Data decompression and pre-processing should be carried out on the compute node rather than the access node to prevent that node from becoming overloaded.
## Environment
---
To ensure consistency across Python environments, venv is designed to guarantee the reproducibility of computations and reduce software development time. In the context of HPC, its use is intended to ensure the optimal utilization of computing clusters and to avoid unusual errors.
## Calculations
---
#### Pre-computation Optimization

Before submitting a workload to the cluster, code must be strictly optimized for parallel processing and efficient hardware utilization. This includes profiling the data input pipeline to prevent CPU bottlenecks, such as adjusting worker counts in deep learning data loaders. Scripts must be validated locally with a minimal sample size to ensure semantic correctness, preventing the waste of allocated computational credits on runtime crashes.

#### Compute Node Enforcement

All active computations, heavy data preprocessing, environment building, and model training must run exclusively on dedicated compute nodes. The login nodes are strictly reserved for text editing, minor file management, and job submission. Running intensive processes directly on access nodes severely disrupts infrastructure availability for other users and violates provider policies.

#### Job Submission and Storage Selection
Jobs are dispatched to the cluster using the SLURM resource manager via batch submission scripts. It is critical to align the workload with the correct storage tier. Configuration files and source code should be kept in the standard directory, whereas active datasets, training logs, and model checkpoints must reside in the high-performance scratch storage to guarantee optimal input-output throughput.

#### Post-computation Workflow

After job completion, developers must inspect the generated output and error logs to confirm successful execution and check hardware efficiency. Validated results, weights, and metrics should be moved to persistent storage, while temporary execution files must be purged from scratch space. Resource utilization statistics should be reviewed to fine-tune allocation requests for future submissions.
