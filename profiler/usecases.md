# Profiler Use Cases

## Simple Profiler Usage

Jimbob has a web-application he wants to analyze to see where it's spending the bulk of its time. He loads the app in his browser and opens the Profiler tool. When the app is in a state that he knows is going to cause some heavy performance loads (beachballs, lack of responsiveness), he clicks the "Start Recording" button and continues interacting with the app. After seeing the expected slow-down, he lets the profiler run for a few more seconds and clicks "Stop Recording".

With a Profile loaded, Jimbob can now see visually in the Stack graph where stack frames were created (depth in Y-axis) over time (X-axis). The graph is color-coded with each color representing a function call (flamechart).

Jimbob looks at the table and sees that the bulk of his sample (88%) was spent in a function called _reallyHorribleLayout(). Jimbob clicks the link to the containing source file and looks at the method in the Debugger.

## Studying a Sample Range

Calamity has recorded a profile of her application running over a period of time. She knows there are some performance issues in here that she'd like to better-understand.

With the Profile loaded, she looks at the Stack graph which shows a repeating pattern of spikes. Between a pair of spikes, there is a small series of bars that don't repeat.

Her first goal is to understand the spikes, so Calamity highlights a range over one of the spikes and selects it in the toolbar. The table of pseudostacks updates to reflect the new highlighted range so Calamity begins expanding entries in the table to see what's causing the spikes to occur. She drills into the table and sees setInterval() and a function called tick().