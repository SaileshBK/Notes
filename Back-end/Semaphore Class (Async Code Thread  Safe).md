## Problem:
Using SemaphoreSlim to make async code thread safe:
This is really useful for limiting only one thread at a time to access the piece of code in a given time. you can use lock key word but not for async. For this we can use Semaphore class for same behavior. 

## Resolution:
// Implementation
var semaphore = new SemaphoreSilm(1);
await SomeTask();


public async Task SomeTask()
{
	await semaphore.WaitAsync();

     try
     {
	     await FinishTask();
     }
     finally
     {
	     semaphore.Release();
     }
}

## Note: 
semaphore.Release(); will prevent potential deadlock.