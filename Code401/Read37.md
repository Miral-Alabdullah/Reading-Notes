# What is Amazon S3?

* Amazon Simple Storage Service (Amazon S3) is storage for the Internet. It is designed to make web-scale computing easier.

<br>

# Advantages of using Amazon S3

**1- Creating buckets** – Create and name a bucket that stores data.

**2- Storing data** – Store an infinite amount of data in a bucket. Each object can contain up to 5 TB of data. Each object is stored and retrieved using a unique developer-assigned key.

**3- Downloading data** – Download your data or enable others to do so. Download your data anytime you like, or allow others to do the same.

**4- Permissions** – Grant or deny access to others who want to upload or download data into your Amazon S3 bucket. Grant upload and download permissions to three types of users. Authentication mechanisms can help keep data secure from unauthorized access.

**5- Standard interfaces** – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.


# Amazon S3 concepts

**1- Buckets:** A bucket is a container for objects stored in Amazon S3. Every object is contained in a bucket.

   * Buckets serve several purposes:
   
     - They organize the Amazon S3 namespace at the highest level.
     
     - They identify the account responsible for storage and data transfer charges.
     
     - They play a role in access control.
     
     - They serve as the unit of aggregation for usage reporting.


**2- Objects:** Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata. The data portion is opaque to Amazon S3. The metadata is a set of name-value pairs that describe the object. 

**3- Keys:** A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key. The combination of a bucket, key, and version ID uniquely identify each object.

**4- Regions:** You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create. You might choose a Region to optimize latency, minimize costs, or address regulatory requirements.

**5- Amazon S3 data consistency model:** Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions. This applies to both writes to new objects as well as PUTs that overwrite existing objects and DELETEs. In addition, read operations on Amazon S3 Select, Amazon S3 Access Control Lists, Amazon S3 Object Tags, and object metadata (e.g. HEAD object) are strongly consistent.