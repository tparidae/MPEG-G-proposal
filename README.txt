Usage:
Java -Xmx16384m -jar Cabacify.jar TASK INPUTFILE/PREFIX MODE

TASK: ENCODE or DECODE. Encoded will by default also run decode and compare the output with the input.
To skip decoding, append nodec to MODE (see below). E.g., Fastnodec will run the fast mode but will skip decoding

INPUTFILE/PREFIX: path to the input file. If the file does not contain an extension, the task will be performed for all valid extensions.
E.g., in case of c:\temp\02_NA12878_S1 the program will, for each extension, append the extension and perform the corresponding compression on all existing files.
E.g., c:\temp\02_NA12878_S1.pair, c:\temp\02_NA12878_S1.mpair, c:\temp\02_NA12878_S1.npair, c:\temp\02_NA12878_S1.gpos ...

MODE: Fast or Ultra. Ultra is the slow mode used in the dissertation.


Note: the large amount of RAM is only required for input and output purposes (buffer, loading files in RAM in case of complex streams such as PAIR), and due to memory inefficient LUT generation.
