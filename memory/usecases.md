# Memory Profiling and Analysis Use Cases

## Measure Allocations

Ruprecht has a web application that he suspects is using a lot of memory. He opens the Memory tool and clicks analyze to generate a table of all of the allocated objects. The graph lists Globals and DOM nodes and their descendants by type, counts, number of references and total sizes of the objects.

Ruprecht was right, his application is using a lot of memory as evidenced by the Total Heap Size display at the bottom of the table. By searching through the Globals section, he discovers an object named ObjectCache which itself contains a large list of objects of objects. Right clicking the object, Ruprecht is able to browse references and definition of this object in his source code in the Debugger and study what the cause of the allocations was.

In this case, it turned out to be an overly-aggressive object caching strategy.

* be nice if the analysis could revcognize the document and display as a folded up thing

* organized by class
** group by allocation site, show total size (+/-)
** sort by size, have retained path

## Memory Consumption at a Glance

Sam wants to see how much memory her application is using. She opens the Memory Widget and sees a running total of how much memory is allocated to her application in the toolbar. Overtime, she can see when garbage collects occur in the widget because of the GC indicator.

## Object Tracing

Dignan is concerned that his application is leaking memory. The memory tools indicate that over time, it seems to keep growing in size. Dignan pushes the button to record Object Allocations and futzes around with his Landscaping web application, creating a new customer and entering their address. When complete, he stops recording and views the allocation graph which shows he's created several new DIVs that are referenced outside of his DOM after the new client was saved (and removed from the page).

## Object Lifetimes

Bree wants to understand the lifetimes of some of the objects in her application. Opening the Object Graph, she is able to see what objects are around at a moment in time. Going back to her application, she does some things, then can measure the heap again and look for objects to see if they're still available.

## Memory Graph Differences

Bree is still trying to determine if her application is consuming resources. She has measured the memory space using the Object graph multiple times so has multiple memory profiles to compare. She selects two of them and applies the Difference command to see what has changed between the two measurements. She can see that one root object has been removed and several new objects have appeared between the two profiles.
