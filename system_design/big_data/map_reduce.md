Large amount of personal data
address, dob, stuff
For each user, redact somme information

Using multiple servers would be faster

- 2 method of processing data
Batch vs Streaming
Batch - All data up front

Streaming - not all data available up front
          - Real time data
          - From a transaction, we want to process something in real time
Batch, run something every week or something

Micro batch - running something every 30 second. More or less in streaming. Input for stream would be message queue

Input data in object storage

If there are multiple servers working, one is designated to be the master

Execute the map step
- The data that we have in an server, Count the occurences of every word
Map is user defined. Programmers will define it

Then we shuffle them.

Map step
Input servers:
[1] - page 1-4
[2] - page 5-8
[3] - page 9-14

shuffle:
Reduce step
Put the counts of each word on their own server. every server will have 1/3 of all data
[1] - Add up 'the'
[2] - Add up 
[3] - 


Modern day batch processing is Spark

