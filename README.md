#### This is working code written in Python to explore the MupB protein sequence, encoded on the mupirocin biosynthetic pathway in ***Pseudomonas fluorescens***. The code can be used to design primers for expression of MupB in ***E. coli*** and calculate GC content of MupB and the selected primers. The code can also be used to calculate the total molecular weight of MupB. The user is free to select a different protein if their interests require.

#### To run: 

1. Download the scripts and fasta file from this repositary in a single directory and ensure the biopython package has been installed in [anaconda.navigator](https://www.anaconda.com/), then launch jupyterlab from the anaconda navigator, the script should open in a jupyter notebook

2. If using the MupB sequence, then continue. If using own protein sequence, then under 'Loading in DNA sequence header' ensure: 
- Download desired protein sequence fasta file from [NCBI](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome) and name appropiately
- Edit line of code SeqIO.read("your-file-name.fasta", "fasta") and label own protein name

3. Run through the next lines of script, but ensure if different protein fasta sequence is read in, that next lines of code are labelled correctly

4. A dictionary of optimised codonds for expression in _E. coli_ has been set up, run the loop in which the empty list mupB_codon = [] is filled with codons defined by the amino acid residues in the mupB sequence. As before, change any appropiate lines of code if a different protein has been selected.
The output of this code, when the filled list has been joined into a string, should be the DNA sequence that encodes the different amino acids in the protein sequence:

![ORF_PIC](https://github.com/Sachacharlton/Data_Science_Assessment/blob/master/Codon_Output.PNG)

5. The next lines of code are used to check that the dictionary and loop functions ran correctly to convert the amino acids into optimised _E. coli codons_. When the codon output has been defined as a new DNA sequence, transcribed and translated into protein sequence, this generated protein sequence can be compared with the original, desired protein sequence to check they match. The 'if' statement in the line of code should then confirm this: 

![if_statement](https://github.com/Sachacharlton/Data_Science_Assessment/blob/master/if_statement.PNG)

6. Use the GC content function to determine the GC content of MupB (or own protein DNA sequence)
 

7. Run the line of code which compliments the MupB DNA sequence (or own protein DNA sequence).

#### To design primer strands:

8. Select the first 6 codons on the forward protein DNA sequence and last 6 codons on the reverse protein DNA sequence. This will be used to design basic primers that can be used to amplify the protein sequence in PCR reaction. This can be appended/edited later with enzyme restriction sites if the DNA sequence was wished to be removed from the original plasmid and ligated to a new desired plasmid.

9. Use the GC function code to determine the GC contents of the selected primer sequences

10. The next line of code uses the original primer sequences, and added EcoRI restriction sites to either the start of the forward primer strand, or the end of the reverse primer strand. These can be edited to different enzyme restriction sites (or appended with extra codons) if desired

11. Use the code below to determine the GC content of these primer sequences with the restriction sites

#### To determine the protein molecular weight: 

12. A dictionary has been set up with the 20 amino acid molecular weights in, this dictionary will be used in a loop to determine the molecular weight of the MupB protein (or own protein). Change the lines of code in the loop for own protein if required
 
13. Use the sum(mupB_mw) code to determine the molecular weight of the MupB protein. Ensure the line above has correctly set the molecular weight list to integers. Change lines of code if necessary for own protein. The output of the code should be the molecular weight:

![mupB_mw](https://github.com/Sachacharlton/Data_Science_Assessment/blob/master/sum_mw.PNG)
