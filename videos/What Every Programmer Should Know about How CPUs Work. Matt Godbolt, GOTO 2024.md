from::Tech Talks Weekly
url::[What Every Programmer Should Know about How CPUs Work • Matt Godbolt • GOTO 2024 - YouTube](https://youtube.com/watch?v=-HNpim5x-IE)
on:: 2025-04-21 08:12

The CPU breaks down instruction processing in pipelines, with decoding and renaming happening sequentially, executing multiple instructions in parallel, and then retiring ("committing" the result of the instruction execution) again happening in sequence.

The modern CPUs have the following pipeline:
- Branch Predict: intelligent guess, will a branch happen, where will it go and whether it will be taken.
- Frontend (in-order):
	- Fetch (read instructions)
	- Decode (decode into internal microops)
	- Rename (rewrite the instructions to avoid data hazards)
- Out-of-order backend: CPU tracks dependencies between the instructions and tries to execute independent instructions in parallel:
	- ROB (Re-order Buffer) Read
	- Execute
	- ROB Write
- Retire (in-order): "commits" the results in program order, handles exceptions.

To make sure we don't need to clean up the whole pipeline on branching, the CPU utilizes branch prediction, however, its technical details are not public (rather reverse-engineered). 
