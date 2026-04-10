1. Compare the results with time quantum 3 and time quantum 5. Which quantum gave better average waiting time? Why?

Time quantum of 5 gave the better avg wait time. If there was a larger quantum ea process gets to run longer before being interrupted so theres less rotations through the queue. What is means is that the processes spend less time waiting to get the CPU back compared to quantum 3, where the CPU switches more often. In this example quantum 5 lets the shorter job finish with less repeated interruptions which improves the avg wait time.

2. What would happen if the time quantum was 1ms? Would the system be more or less efficient?
If the time quantum was 1ms the sys would switch between processes very frequently. That would make the scheduling feel very fair because every process gets CPU time quickly but it would also create more context switches. Due to that, the sys would be less efficient overall since more time would be spent switching between processes insead of actually doing useful work. So it improves responsivenesss but hurts efficiency. 

3. What would happen if the time quantum was 20ms (larger than any process burst time)? How would Round Robin behave then?
If the time quantum was 20ms which is larger than every burst time in the example, then ea process would finish in its first turn. If thats the case then Round Robin would act almost the same as first come first served because no process would need to be placed back into the queue. Ea one would run to completion in the order it appears so the preemptive part of Round Robin would basically disappear. 

4. In the simulation with quantum 3, how many context switches occurred? Count each time a process was removed from the queue.
P1 runs for 3 ms, remaining 4
P2 runs for 3 ms, remaining 1
P3 runs for 2 ms, finished
P1 runs for 3 ms, remaining 1
P2 runs for 1 ms, finished
P1 runs for 1 ms, finished

That means a process was removed from the queue 6 times so there were 6 context switches using the way the question defines it

5. Why does Round Robin prevent the convoy effect that occurs in FCFS scheduling?
Round Robin prevents the convoy effect because one long process cannot keep the CPU for too long. In first come first serve, if a VERY large job gets the CPU first all the shorter jobs get stuck waiting behind it, which creates a convoy of delayed processes. In Round Robin, every process only gets to CPU for one time quantum before being moved aside so that smaller jobs still get chances to run quickly. This keeps the system more balanced and responsive. 
