# FASTQ File Format

`Fastq` files hold sequencing data in 'reads'. Each read has a description, a sequence, and a quality sequence.

What Fastq looks like (downloaded from [Pseudomonas aeruginosa MPAO1/P1 variant](https://trace.ncbi.nlm.nih.gov/Traces/sra/?run=SRR396637), direct download from (ENA)[ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR396/SRR396638/SRR396638.fastq.gz]):

    @SRR396638.1 0370:3:1:1320:948/1
    NCCGGCCCCCTGGGCGGTCACCTACGGCCCATCGAC
    +
    #-,-255222@@@@######################
    @SRR396638.2 0370:3:1:1541:939/1
    NTCGACCACCCAGACCCTCGGAGGCGGCTTCGGCAA
    +
    ####################################

These are the first two reads from the `fastq` file from sequencing a variant of *Pseudomonas aeruginosa*. The description starts with `@`. 

In our description we have the [NCBI SRA read run](https://www.ncbi.nlm.nih.gov/sra) and other information about the data that's specific to the methods used to generate the data.

Next, we have the actual sequence of the reads and (separated by a `+` and a few returns) the quality sequence of the read. The first sequence starts with `NCCGG`, and the first five quality encoding characters are `#-,-`.

Quality encoding is a [whole thing in itself](../Index/Quality_Encoding.md), read more about it in the index!