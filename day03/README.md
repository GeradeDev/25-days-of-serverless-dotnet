## Day 3 - Storage Trigger

Web service that lets users upload photos, but then verifies that each uploaded photo/file is a png. If it is not, delete the photo. (storage trigger)

### Solution

* Azure HTTP triggered function with Blob output binding that exposes an endpoint for upload \[POST\] http://localhost:7071/api/photo/{filename} 
* Azure Blob Storage triggered function that deletes the blob if it doesn't have a PNG header.
