# 25-days-of-serverless-dotnet

Dotnet implementation of 25 days of serverless

## Day 1 - A Basic Function

REST API endpoint that spins a dreidel and randomly returns נ (Nun), ג (Gimmel), ה (Hay), or ש (Shin).

 Azure Function that exposes an endpoint: \[GET\] http://localhost:7071/api/spin

 ## Day 2 - Task Scheduler

Task scheduler that will tell Lucy exactly when she should relight candles, pour coffee into cups, and deliver batches of coffee.

 Durable function that runs annually on December 13 at 8:00 AM local server time (0 0 8 13 12 *) and uses Durable Timers in between tasks.