# Biological File Types

Biological data is packaged in file types for targeted purposes. If a variant analysis was done, we might get back a variant call file ([VCF](https://en.wikipedia.org/wiki/Variant_Call_Format)), which will annotate variants from a genome reference. Sequencing Alignment Mapping ([SAM](https://en.wikipedia.org/wiki/SAM_(file_format))) files are usually a lot larger and contain all the sequencing data aligned to our genome reference. [Fasta](https://en.wikipedia.org/wiki/FASTA_format) files (not really short for anything) are the simplest of all; they only contain sequences and descriptions of the sequences.

## Background

[Official File Format Specifications](http://samtools.github.io/hts-specs/). Includes VCF,  SAM, CRAM, BAM, BCF, CSI, Tabix, crypt4gh, htsget, and Refget

What VCF data looks like:
```
#CHROM POS
20 14370 20 17330 20 1110696 20 1230237 20 1234567
ID REF rs6054257 G
. T rs6040355 A
. T microsat1 GTC
ALT QUAL FILTER A 29 PASS
A 3 q10 G,T 67 PASS
. 47 PASS G,GTCT 50 PASS
INFO
NS=3;DP=14;AF=0.5;DB;H2 NS=3;DP=11;AF=0.017 NS=2;DP=10;AF=0.333,0.667;AA=T;DB NS=3;DP=13;AA=T
NS=3;DP=9;AA=G
FORMAT GT:GQ:DP:HQ GT:GQ:DP:HQ GT:GQ:DP:HQ GT:GQ:DP:HQ GT:GQ:DP
NA00001 0|0:48:1:51,51 0|0:49:3:58,50 1|2:21:6:23,27 0|0:54:7:56,60 0/1:35:4
NA00002 1|0:48:8:51,51 0|1:3:5:65,3 2|1:2:0:18,2 0|0:48:4:51,51 0/2:17:2
NA00003 1/1:43:5:.,. 0/0:41:3 2/2:35:4 0/0:61:2 1/1:40:3
```