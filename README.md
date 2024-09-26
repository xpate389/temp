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
Download Datasets

Steps to Setup the Dataset
Download the datasets and save them in the datasets directory. Create the directory if it doesn’t exist:

bash

```mkdir datasets
```
Copy the dataset to the remote machine and unzip it:

```bash
scp Dataset1.zip cc@<remote-ip>:<path-to-repo>/datasets/.
cd <path-to-repo>/datasets
unzip Dataset1.zip
```


How to Build and Run the Java Solution
Build Instructions:
To compile and build the project, follow these steps:

Navigate to the app-java directory:

```bash
cd app-java
```
Compile the project:

```bash
mvn compile
```

Package the project into a JAR file:

```bash
mvn package
```

Run Instructions:
After building the project, use the following command to run the file retrieval engine:

```bash
java -cp target/app-java-1.0-SNAPSHOT.jar csc435.app.FileRetrievalEngine <number of worker threads>
```


For example, to run the application with 4 worker threads:

```bash
java -cp target/app-java-1.0-SNAPSHOT.jar csc435.app.FileRetrievalEngine 4
```

Commands
Once the application starts, you can use the following commands:

Index a Dataset:

```bash
> index <path-to-dataset>
```

Example:

```bash
Copy code
> index ../datasets/Dataset1
```

Search for a Term:

```bash
Copy code
> search <term>
```

Example:

```bash
Copy code
> search Worms
```

Search for Multiple Terms (AND):

```bash
Copy code
> search <term1> AND <term2>
```

Example:

```bash
Copy code
> search distortion AND adaptation
```


Quit the Application:

```bash
> quit
```

Example Output
Indexing:
```bash
> index ../datasets/Dataset1
Completed indexing using 4 worker threads
Completed indexing 192889895 bytes of data
Completed indexing in 8.251 seconds
```

Searching for a Single Term:
```bash
> search Worms
Search completed in 3.2 seconds
Search results (top 10):
* Dataset1/folder6/document200.txt 10
* Dataset1/folder14/document417.txt 3
* Dataset1/folder6/document424.txt 3
* Dataset1/folder11/document79.txt 1
```

Searching for Multiple Terms:
```bash
> search distortion AND adaptation
Search completed in 4.52 seconds
Search results (top 10):
* Dataset1/folder6/document200.txt 46
* Dataset1/folder13/document38.txt 4
```

Troubleshooting
If you encounter any issues during the build or execution, consider the following:
Ensure all required software is installed and properly configured.
Verify the paths to the datasets are correct.
Check the command syntax for errors.
For more detailed error messages, run Maven with the -e or -X switches for debugging.



Contact Information
For any questions or issues, feel free to contact me at:
Email: TO-DO-write-email-address
