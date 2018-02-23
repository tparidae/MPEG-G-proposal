Usage:
Java [-XX:+UseG1GC] -jar MPEG-G.jar TASK INPUTFILE/PREFIX MODE

TASK: ENCODE or DECODE. Encoded will by default also run decode and compare the output to the input.
To skip decoding when ENCODE is selected, append nodec to MODE (see below). E.g., Fastnodec will run the fast mode but will skip decoding

INPUTFILE/PREFIX: path to the input file. If the file does not contain an extension, the task will be performed for all valid extensions.
E.g., in case of c:\temp\02_NA12878_S1 the program will, for each extension, append the extension and perform the corresponding compression on all existing files.
E.g., c:\temp\02_NA12878_S1.pair, c:\temp\02_NA12878_S1.mpair, c:\temp\02_NA12878_S1.npair, c:\temp\02_NA12878_S1.gpos ...

MODE: Fast or Ultra. Ultra is the slow mode used in the dissertation.

Note: -XX:+UseG1GC enables the G1 Garbage Collector. This garbage collector offers higher efficiency regarding releasing unused Heap Space (hence, RAM) at a speed penalty.
