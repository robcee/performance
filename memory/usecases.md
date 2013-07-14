# Memory Profiling and Analysis Use Cases

## Measure Allocations

Ruprecht has a web application that he suspects is using a lot of memory. He opens the Memory tool and clicks analyze to generate a table of all of the allocated objects. The graph lists Globals and DOM nodes and their descendants by type, counts, number of references and total sizes of the objects.

Ruprecht was right, his application is using a lot of memory as evidenced by the Total Heap Size display at the bottom of the table. By searching through the Globals section, he discovers an object named ObjectCache which itself contains a large list of objects of objects. Right clicking the object, Ruprecht is able to browse references and definition of this object in his source code in the Debugger and study what the cause of the allocations was.

In this case, it turned out to be an overly-aggressive object caching strategy.

## Object Tracing

Dignan is concerned that his application is leaking memory. The memory tools indicate that over time, it seems to keep growing in size. Dignan pushes the button to record Object Allocations and futzes around with his Landscaping web application, creating a new customer and entering their address. When complete, he stops recording and views the allocation graph which shows he's created several new DIVs that are referenced outside of his DOM after the new client was saved (and removed from the page).

## Object Lifetimes

## Memory Graph Differences

## Memory Consumption at a Glance