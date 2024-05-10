The goal for this project is to creat code that can be applied to any fasta file that can take in csv of significant sites as input to search for M5C methylation sites and the corresponding nucleotide sequences.
This project will parse through a fasta file for Heliobacter pylori and extract sequences of interest that have been shown to be sites of M5C methylation. 
  First the script will create a list of significant sites from the CSV called SRR15720537_primrose_condifent_sites.csv. This csv contains specific sites that have been flag as possible locations sites within the genome that have been methylated. 
  Next, using the list of significant site ids, the next function will loop through the list as well as parse through the fasta file and based on each significant site ids, extract nucleotides upstream and downstream of 20 nucleotide. 
  The outpute of this script will be be written out to a file called output.fasta which will contain the specific ID location and nucleotide sequence of interests.  
packages needed for this code: 
from Bio import SeqIO
from Bio.SeqRecord import SeqRecord
import csv
import pandas as pd 
