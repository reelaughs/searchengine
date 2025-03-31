# searchengine
Group project for NTU MSc in Information Systems, Information Retrieval and Analysis module

The overall assignment, split into 3, was to write a software system.
We were first tasked to create the indexing component of an information retrieval system using one of the external sorting algorithms that were discussed in class: BSBI or SPIMI.
As an input to the system, the system was required to take 
(I) path to the directory containing the text files to index; 
(II) block size parameter for BSBI/SPIMI. 
The output of the algorithm was required to be a single text file containing a sorted list of term-document pairs.

We were also tasked to produce reports indicating the time taken to index the whole dataset, to sort a block, to merge blocks, etc. 
We also measured how much memory the application required and whether it was consistent with the block size parameter. 

Other constraints/requirements:
1) We had to make sure that the system never read more at once, more than the block size stipulated as an input parameter.
2) Tokens could only be split on whitespace characters (space, newline, tab).
3) To not create empty tokens (there could be several whitespace characters in a row) 

Directory Listing
Input: string (path to directory)
Output: list of strings (full paths to files in the directory)
This component will list all the files (with full paths) in the directory. This will simplify going through the files at the indexing stage.
File Reading
Input: string (full path to file)
Output: string/text (full contents of a file)
Some programming languages have this function in the standard library, some do not. It will be very useful to have this functionality easily accessible in this project, so either find it in the standard library of your programming language or write a small function that does that.
Tokenisation
Output: pairs <token, document>
Note that you cannot output a full list of tokens at one because it may be larger than the block size. One approach may be to output pairs one by one with each call to the tokeniser component.

Overall initial structure:

**Directory Listing**
Input: string (path to directory)
Output: list of strings (full paths to files in the directory)

**File Reading**
Input: string (full path to file)
Output: string/text (full contents of a file)

**Tokenisation**
Output: pairs <token, document>

**Linguistic Modules**
Input: pairs <token, document>
Output: pairs <modified token, document>
The python implementation of Porter Stemmer nltk was used. 



