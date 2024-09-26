# CSC 435 Programming Assignment 3 (Spring 2024)

**Jarvis College of Computing and Digital Media - DePaul University**

**Student:** TO-DO-write-student-name  
**Email:** TO-DO-write-email-address  
**Solution Programming Language:** Java  

---

## Project Overview

This project is a file retrieval engine implemented in Java. The application uses an `IndexStore` to build an index of terms from a dataset of documents and allows users to search for specific terms using multi-threaded processing. 

The application supports:
1. **Indexing** large datasets across multiple threads.
2. **Searching** for terms in the indexed documents and returning the top results.
3. An interactive command-line interface for indexing, searching, and quitting.

---

## Requirements

You will need the following software installed on your system to run this solution:

- **Java 17.x**  
- **Maven 3.6.x**

On Ubuntu 22.04 LTS, you can install Java and Maven using the following commands:
```bash
sudo apt install openjdk-17-jdk maven
```

###Setup
There are 5 datasets (Dataset1, Dataset2, Dataset3, Dataset4, Dataset5) that are used to evaluate the indexing performance. You can download the datasets from the following link:
