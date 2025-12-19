Newer than file system
Much more comparable to file system rather than database

Data stored in flat way, no folders or any of that
AWS S3, GCS, MinIO

S3 can have folders and files and things in them. All the things are actually stored in a flat way

Binary large object (BLOB)
images, videos

When we put objects in object storage, cannot update the things we add
Kinda like a hashmap
Cannot have duplicates
Need globally unique names

Imgs/videos could be stored in database
Would we ever query on img or video? 
Can store metadata in databases, but files in a flat way

Dont need to filter anyhting or look at anything, can just make a request to the s3 things
Just knowing the file name we can store it
