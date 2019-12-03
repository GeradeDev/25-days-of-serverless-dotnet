# 25-days-of-serverless-dotnet

Dotnet implementation of 25 days of serverless

## Day 1 - A Basic Function

REST API endpoint that spins a dreidel and randomly returns נ (Nun), ג (Gimmel), ה (Hay), or ש (Shin).

### Solution

Azure HTTP triggered Function that accepts a request for a spin result: \[GET\] http://localhost:7071/api/spin

## Day 2 - Task Scheduler

Task scheduler that will tell Lucy exactly when she should relight candles, pour coffee into cups, and deliver batches of coffee.

### Solution

Azure Timer triggered Durable function that runs annually on December 13 at 8:00 AM local server time (0 0 8 13 12 *) and uses Durable Timers in between tasks.

## Day 3 - Storage Trigger

Web service that lets users upload photos, but then verifies that each uploaded photo/file is a png. If it is not, delete the photo. (storage trigger)

### Solution

Azure HTTP triggered function that exposes an endpoint for upload \[POST\] http://localhost:7071/api/photo/{filename} 
Azure Blob Storage triggered function that deletes the blob if it doesn't have a PNG header.