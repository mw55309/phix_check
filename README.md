# phix_check
A simple Perl script to check for PhiX174 contamination in fastq data

The script will:

1. Check for BWA
2. If BWA is present, it will check if it can run BWA MEM
3. If BWA is not present, or MEM is not enabled, it downloads and installs BWA to the current working directory
4. So you need write access to the current working directory...
5. It then downloads PhiX174 genome
6. And builds a BWA index
7. It then takes the top n reads from a fastq file (gzipped or raw) and counts how many map to PhiX
8. Relies on bash

n is currently set to 10,000

Usage:

perl phix reads.fastq

Email: mick.watson@roslin.ed.ac.uk

FEEDBACK
--------

I wrote this in 30 minutes whilst my baby was vomiting all over Mummy, as a joke-ish script, see: https://biomickwatson.wordpress.com/2015/04/21/excited-by-bacterial-dna-in-sweet-potatoes-check-this-out/

Are you whining about the script?  If you're from Dundee - it's expected, please carry on :-)  If you're not from Dundee, feel free to improve it :-)


