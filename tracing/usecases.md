# Tracer Use Cases

## Function Execution Tracing

Cynthia as a result of some Profiling, has a function that she suspects is being called frequently and is consuming a lot of time. She runs the Tracer while interacting with her application to analyze it. Cynthia can now analyze the trace and Search for invocations of the function in question to better understand the application flow.

When she has some search results, she is able to navigate through the Trace and view the highlighted matches in context.

## Code Coverage in Debugger

Paul is running his unit tests in the browser. He wants to know how much of his code is being run by his tests as a general measure of how well his code is tested. He uses console.traceCalls() at the start of his tests and console.stopTracing() at the end. The debugger's source editor highlights the functions that have been run during the tests. By looking at what has been run and what hasn't Paul can decide where to focus his efforts of writing more tests or improving existing ones.

## STR Tracing

Linda has found a bug in her application. She deploys the Tracer and reruns her steps to reproduce the bug. When complete, she can stop the tracer and export it for upload to the bug in her issue tracker. Now Rob (a developer working on the app) can import the trace into his Tracer and quickly narrow down the function where the bug occurs and what arguments to that function might have triggered the bug.

## Object Allocation Points [??]

Gerhardt  is curious about what parts of his application are allocating the bulk of his memory. He starts a Tracer and uses the application for awhile. When finished, he looks at the generated Trace and searches for  allocations.

* Take a snapshot of scope at entry and exit and compare differences

* Search for FooObjectFactoryFactory instances and highlight all calls where they were allocated

## Statistical Analysis - [may be better served by the Profiler]

* How many times you enter a function
* Number of allocations
* Percentage of time inside each function
