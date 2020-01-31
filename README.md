# Big_Data
## Module overview 
This module covers what constitutes big data and how it’s handled. We’ll start by reviewing Hadoop and its ecosystem.
Within this big data and Hadoop context, we'll cover MapReduce and how it has improved the process for handling big data. We’ll then move on to PySpark, which has become the leading technology for handling big data.
After diving into some of the technologies used with big data, we'll look at natural language processing (NLP) in relation to big data.
We’ll close with an introduction to cloud services. Cloud services let us store large amounts of data at remote locations rather than locally, on top of many other services. This allows for more scalability and performance. We’ll use the most popular cloud service available: Amazon Web Services (AWS).
## Objectives
•	Define big data and describe the challenges associated with it.
•	Define Hadoop and name the main elements of its ecosystem.
•	Explain how MapReduce processes data.
•	Define Spark and explain how it processes data.
•	Describe how NLP collects and analyzes text data.
•	Explain how to use AWS Simple Storage Service (S3) and relational databases for basic cloud storage.
•	Complete an analysis of an Amazon customer review.

### Four Vs of Big Data
There are four characteristics of big data:
+	Volume refers to the size of data (e.g., terabytes of product information). For instance, a year’s worth of stock market transactions is a large amount of data.
+	Velocity pertains to how quickly data comes in (customers across the world purchasing every second). As an example, McDonald’s restaurants are worldwide with customers buying food at a constant rate, so the data comes in fast.
+	Variety relates to different forms of data (e.g., user account information, product details, etc.). Consider the breadth of Netflix user information, videos, photos for thumbnails, and so forth.
+	Veracity concerns the uncertainty of data (e.g., reviews might not be real and could come from bots). As an example, Netflix would want to verify whether users are actively watching the shows, falling asleep, or just playing them in the background.
The four Vs of big data will help you determine when to migrate from regular data to big data solutions.
Big Data Problems
Working with datasets of this size creates unique challenges. How will we store all of this data? How can we access it quickly? How do we back up this type of data?

## Summary
Apache Hadoop (Hadoop) is one of the most popular open source frameworks, with numerous technologies for big data. Google developed Hadoop to process large amounts of data by splitting data across a distributed file system.
We’ll start with the three main components of Hadoop:
+	Hadoop Distributed File System (HDFS) is a file system used to store data across server clusters (groups of computers). It is scalable (which means it handles influxes of data), fault-tolerant (handles hardware failure), and distributed (spread across multiple servers connected by a common core).
+	MapReduce is a programming model and processing technique for big data. MapReduce enables processing the large amount of data spread across the cluster in the HDFS by performing the same task for each file system.
+	Yet Another Resource Negotiator (YARN) manages and allocates resources across the clusters and assigns tasks.
Hadoop distributes for the storage and processing of data through a cluster, which is a group of connected computers that work together to store and perform tasks on a dataset.

## MapReduce Process
MapReduce is used as a means for distributing and processing data on your cluster. MapReduce is built on the process of mapping—the process of assigning the same job to each of the computers—and reducing, which is when you come back together to combine the results.

By splitting up the data, the time to analyze it has been reduced by half. In the same way, MapReduce works on divided datasets in smaller batches so that we can work faster.
Once you are done, you will come together and combine the tallies for both.
Mapping is taking a small piece of the input and then converting the data into key-value pairs, with key identifiers and associated values.
Key Features of Spark
Hadoop is an ecosystem for handling big data. Expect to spend significant time configuring multiple servers or computers, as well as researching which technology can best deliver your big data solution. With the growing interest in big data and the ease of access to cloud technology, which we’ll cover later, Hadoop is no longer required. New technologies allow more flexibility in data processing. One of these technologies is Spark.

### Apache Spark (Spark) 
is a unified analytics engine for large-scale data processing. Spark lets you write applications in code that can run on Hadoop. However, Spark doesn’t have to run on Hadoop, as it can run in stand-alone mode or in the cloud. Spark can be 100 times faster than Hadoop. Just like Hadoop’s MapReduce, Spark works with data spread across a cluster, or a group of computers that work together.
Spark uses in-memory computation instead of a disk-based solution, which means it doesn’t need to talk to the HDFS each time and can retain as much as HDFS can in-memory. Spark uses lazy evaluation, which delays the evaluation of an expression or command until the value is needed.
For example, when you direct Spark to count all the product reviews and then group them by star rating, Spark is ready to start, but you’ll need to initiate the task—at this point, no counting or grouping has been done, only the instructions have been given. Once you give the go-ahead, Spark will then count and group the reviews all at once.
The Spark architecture includes the driver, executors, and the cluster manager:
+	The driver is the heart of the application. It is responsible for maintaining the application information; responding to the code or input; and analyzing, distributing, and scheduling work to the executors.
+	The executors perform the code assigned by the driver and then report the state of the computation to the driver.
+	The cluster manager controls the driver and executors and allocates resources to the machines on the Spark applications. The cluster manager is an external service for acquiring resources on the cluster. Spark can either use it’s own standalone cluster manager that comes standard with Spark or another application (e.g., Apache Mesos, Hadoop YARN).

## Natural language processing (NLP) 
is a growing field of study that combines linguistics and computer science for computers to understand written, spoken, and typed natural language. NLP is the process of converting normal language to a machine readable format, which allows a computer to analyze text as if it were numerical data.
While NLP has a wide variety of use cases, and the field is rapidly growing, there are a few use cases that are particularly interesting:
•	Analyzing legal documents: NLP can be used to analyze many types of legal documents. This can improve the outcome of a given case, as lawyers and staff can find critical information quickly.
•	U.S. Securities and Exchange Commission (SEC) filings: NLP is used to analyze SEC filings for various businesses. Companies use NLP to analyze filings for real-time business intelligence.
•	Chatbots: Chatbots are one of the most popular use cases. Chatbots can be used for selling products, customer support, and even medical help.
At this point, you might ask how this relates to big data. Due to the massive amounts of text data needed to drive insights, we'll have to learn how to manage that data. There are a number of important use cases to delve into:
•	Classifying text: For many of the aforementioned use cases to work, a computer must know how to classify a given piece of text. Classification can mean a few different things in NLP. You can have classification of specific words, even specifying what the part of speech is. You can also classify what the text is as a whole.
•	Extracting information: Many NLP tasks require the ability to retrieve specific pieces of information from a given document. Think of the case where we are extracting data from law documents. You might want to extract certain aspects of that document to present good cases.
•	Summarizing a document: Summarization is a key aspect of NLP. It helps solve quite a few different problems. You can essentially create a model that summarizes a given document. This can be helpful to understand the high-level details of law documents, articles, and much more.
###  Natural Language
Natural language can be complicated because the way it’s written is not always how it is intended. Therefore, you might need the full context to understand the meaning.
Sarcasm is a great example. Say you had a bad experience at a restaurant. Your friend asks if you liked your meal and you reply “Oh, yeah, the food was amazing if you like dry, bland food.” A friend familiar with your humor would understand your true intentions behind the quip. However, a straight reading, without detecting sarcasm, would give the impression you prefer dry, bland food.
Another challenge is interpreting the tone behind the text. For instance, snidely remarking “Great” and enthusiastically exclaiming “Great!” reveal two distinct tones but, in text, it is the same word.

These are just two examples of the complexity of dealing with natural language. In the next section, we'll show how a computer does its best to interpret language.
 Computers Understanding Language
Computers comprehend language differently than humans do, so you have to teach the computer how to understand natural language.
On a fundamental level, the computer processes information as 1s and 0s. Machine-level programming languages, which are simple programming languages, process those 1s and 0s and can perform simple operations. Higher-level programming languages execute more complex tasks. Each programming language builds on one another. This high-level overview explains in part what happens when a computer processes language.
We need NLP so that computers can better analyze language and someday communicate seamlessly with humans. Despite significant advancements in NLP, computers still struggle to understand the whole context of a text. For now, they just understand definitions and the literal meaning of a text. They don’t understand sarcasm or subtext or anything not explicitly defined or expressed.

### Tokenization
Tokenization is the concept of splitting a document or sentence into small subsets of data that can be analyzed. It’s essentially the building block of most NLP use cases. Tokenization can be performed by word or sentence.
To tokenize by word, you take a given sentence or document and split it into a list of words, with each sentence or word representing a token. A sentence tokenized by word would look like the following:
Original sentence: I am enjoying learning about NLP.
Tokenized by word: ['I', 'am', 'enjoying', 'learning', 'about', 'NLP', '.']
### Normalization
Normalization is the concept of taking misspelled words and converting them into their original form. This is another building block in NLP in that it helps get the text to a readable form and allows us to create other use cases on top of it. Essentially, it makes it easier for us to create NLP programs, and it improves the output of those programs. There are numerous ways to accomplish this, but we’ll focus on just two practices: stemming and lemmatization. Stemming and lemmatization are similar in that they both remove the suffix from a word, but there are some differences in how smooth or rough the cutoff tends to be:
•	Stemming removes the suffix from a word and reduces it to its original form. This serves as a “rough” cut off of the end of the word.
•	Lemmatization removes the suffix from a word and reduces it to its original form. Lemmatization tends to be a “smoother” cut off of the end of the word. It tries to return to the original root word.
Explain how to use AWS Simple Storage Service (S3) and relational databases for basic cloud storage.
S3 is Amazon’s cloud file storage service that uses key-value pairs. Files are stored on multiple servers and have a high rate of availability of more than 99.9%. To store files, S3 uses buckets, which are similar to folders or directories on your computer. Buckets can contain additional folders and files. Each bucket must have a unique name across all of AWS.
+	One of S3’s perks is its fine-grained control over files. Each file or bucket can have different read and write permissions, which helps regulate what can be done with each file.
+	S3 is also very scalable—you are not limited to the memory of one computer. As data flows in, more and more can be stored, as opposed to a local computer that is limited by available memory.
+	Additionally, it offers availability—several team members can access massive amounts of data from one central location.
## Challenge Overview
Complete an analysis of an Amazon customer review.
Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. However, they are quite large and can exceed the capacity of local machines to handle. One dataset alone contains more than 1.5 million rows. With more than 40 datasets, this can be quite taxing on the average local computer.
## Challenge Objectives
+	Perform ETL on one of the review datasets.
+	Store your results on an AWS RDS database.
+	Determine if reviews are biased using PySpark or SQL with the appropriate statistical methods.
## Challenge Summary
Instructions
1+) Use the furnished schemata to create tables in our RDS database.
2+) Create a Google Colab Notebook and extract any dataset from the list of review datasets , one into each notebook.
3+) For the notebook, complete the following:
+	Extract the dataset from the S3 bucket and load into a DataFrame.
+	Count the number of records (rows) in the dataset.
+	Transform the dataset to fit the tables in the schema file.
+	Load the DataFrames that correspond to tables into an RDS instance.
4+) Use either PySpark or SQL to analyze the data and determine if the Vine reviews are biased.
+	If you choose to use SQL, use the vine_table from the result of the previous step. Perform your analysis with SQL queries on RDS.
+	If you choose to use PySpark, create a new notebook and perform your analysis there.
+	Consider steps to take to reduce noisy data.
