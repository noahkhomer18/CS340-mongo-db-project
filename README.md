# MongoDB Client-Server Development Assignment

## Project Overview
This repository contains the MongoDB assignment for the **CS 340 - Client-Server Development** course. The objective of this project is to gain hands-on experience with MongoDB commands and administrative functions using a dataset of email documents (`enron.json`). This assignment involves setting up MongoDB, importing data, executing queries, and performing administrative tasks in a Linux terminal environment.

## Key Tasks
The main tasks accomplished in this project are:
1. **Accessing the MongoDB Shell**: Establishing a connection to MongoDB via the Linux terminal.
2. **Importing the Enron Email Dataset**: Loading the `enron.json` file into MongoDB’s `emails` collection.
3. **Database and Collection Verification**: Ensuring access to the `enron` database and confirming the presence of the `emails` collection.
4. **Document Retrieval**: Querying a sample document from the `emails` collection.
5. **Calculating Document and Collection Sizes**: Using MongoDB commands to determine the size of individual documents and the entire collection.

## Technologies Used
- **MongoDB**: Database management system for handling document-based data.
- **Linux Terminal**: Command-line interface to interact with MongoDB.
- **Mongo Shell**: Tool for executing MongoDB commands and queries.

## Commands Overview
Below are the key commands used in this assignment, which are useful for managing and querying data within MongoDB:

1. **Access MongoDB Shell**:
   ```bash
   mongo
This command starts the Mongo shell, allowing you to interact with MongoDB.
cd /usr/local/datasets
mongoimport --username="${MONGO_USER}" \
    --password="${MONGO_PASS}" --port=${MONGO_PORT} \
    --host=${MONGO_HOST} --db enron --collection emails \
    --authenticationDatabase admin --drop ./enron.json
This command imports the enron.json dataset into the enron database’s emails collection.
show dbs
Lists all available databases to confirm the presence of enron.
use enron
Sets the current database to enron.
show collections
db.emails.findOne()
Object.bsonsize(db.emails.findOne())
db.emails.stats()
Screenshots
Screenshots of each command and output are provided in the screenshots folder for reference. Each screenshot includes a visible username to meet course requirements.

Key Learnings
This assignment provided valuable experience with:

MongoDB Setup and Management: Importing datasets, creating collections, and performing queries.
Administrative MongoDB Commands: Working with mongoimport, findOne(), and stats() commands to manage data.
Linux Terminal Proficiency: Executing MongoDB commands and navigating the command-line interface efficiently.
How to Use
To replicate the MongoDB setup and commands in this repository:

Clone this repository:
bash
git clone https://github.com/your-username/mongo-client-server-assignment.git
Navigate to the repository:
bash
cd mongo-client-server-assignment
Follow the commands in the Commands Overview section above to interact with MongoDB and perform the tasks.
License
This project is for educational purposes as part of the CS 340 course and is licensed under the MIT License.


