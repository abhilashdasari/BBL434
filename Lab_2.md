# Lab session 2
## This lab is mainly focussed on Regular expression and MEME

It is important to learn basic BASH (mainly usage of `grep`, `awk`, `sed` ) for efficient use of Regular expression

### task 1 : Quickly watch this video in 1.5x and understand How shell scripting works, how to write functions and loops

To learn bash go through this video (3 hrs) which starts from basic bash [Bash scripting Video link](https://www.youtube.com/watch?v=e7BufAVwDiM "Bash scripting")

While watching the video mainly focus on 

### task 2 : Examples for regex patterns
To learn Regular expressions `grep`, `awk`, `sed` [grep, awk and sed video link](https://www.youtube.com/watch?v=e7BufAVwDiM](https://www.youtube.com/watch?v=KJG1dETacLI) "Bash scripting")

To learn specialised REGEX pattern examples [Video]([https://www.youtube.com/watch?v=KJG1dETacLI])

From the above videos you learnt
* BASH scripting
* Regex patterns

Now we will apply the knowledge gained in Life science


### task 3 : Understanding the importance of grep with regex using bioinformatics examples [link](https://bioinformaticsworkbook.org/Appendix/Unix/unix-basics-3grep.html#gsc.tab=0)

### task 4 : Understanding the importance of sed with regex using bioinformatics examples [link](https://bioinformaticsworkbook.org/Appendix/Unix/unix-basics-4sed.html#gsc.tab=0)

### task 5 : Understanding the importance of awk with regex using bioinformatics examples [link](https://bioinformatics.cvr.ac.uk/essential-awk-commands-for-next-generation-sequence-analysis/)


After understanding above grep, sed, awk examples, visit this cheat sheet
[Regex cheet sheet](https://cheatography.com/davechild/cheat-sheets/regular-expressions/)
Check wether you are familier with all the 
* Anchors
* Character class
* Quantifiers
* Escape characters
* String replacements
* Groups and ranges

## Practice questions 

1. Search for a restriction digestion enzyme, pick its restriction digestion site sequence, find how many times the restriction enzyme sites are present in the E.coli genome
EcoRI- GAATTC

#### Hint
* Download Ecoli genome in fasta format [here](https://www.ncbi.nlm.nih.gov/genome/?term=E+coli)
* search using grep

2. [Regular expressions for biologists](https://carpentries-incubator.github.io/regex-novice-biology/03-tokens-and-wildcards/index.html)

3. Assume a biologist come to you with a file of >1000 coding sequences of a prokaryote, asks you to pick ORF region for each gene. How do you pick the ORF sites

File consists of sequences like
```
>lcl|LR794089.1_cds_CAB3563250.1_1 [gene=mutS] [protein=Methyl-directed mismatch repair] [frame=2] [protein_id=CAB3563250.1] [location=<1..>498] [gbkey=CDS]
CGCCATCCGGTGGTTGAACAGGTACTGAACGAGCCATTTATCGCCAACCCGCTGAACCTGTCGCCGCAGC
GTCGCATGTTGATCATTACCGGTCCGAATATGGGCGGTAAAAGTACCTATATGCGCCAGACCGCACTGAT
TTGTTTGCTACCCATTATTTCGAGCTGACCCAGTTACCGGAGAAAATGGAAGGCGTGGCTAACGTGCATC
TCGATGC

>lcl|LR794088.1_cds_CAB3563248.1_1 [gene=mutS] [protein=Methyl-directed mismatch repair] [frame=2] [protein_id=CAB3563248.1] [location=<1..>498] [gbkey=CDS]
CGCCATCCGGTAGTTGAACAAGTACTGAATGAGCCATTTATCGCTAACCCGCTGAATCTGTCGCCGCAGC
GCCGTATGTTGATCATCACCGGTCCGAACATGGGCGGTAAAAGTACCTATATGCGCCAGACCGCGTTGAT
CTGTTTGCCACCCACTATTTCGAGCTGACACAGTTACCGGAGAAAATGGAAGGCGTCGCCAACGTGCATC
TCGATGC
```
#### Hint
* First linerarize the fasta which means print header in one line, then print sequence in one line 
```
>lcl|LR794089........
CGCCATCCGGTGGTTGAA......
>lcl|LR794088.1_.......
CGCCATCCGGTAGTT.........
```
* using the logic the coding sequence starts with ATG and ends with stop codon TAA or TAG or TGA. try too pick the lines beteen start codon and stop codon using grep

