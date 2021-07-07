# Biological File Types

Biological data is packaged in file types for targeted purposes. If a variant analysis was done, we might get back a variant call file ([VCF](https://en.wikipedia.org/wiki/Variant_Call_Format)), which will annotate variants from a genome reference. Sequencing Alignment Mapping ([SAM](https://en.wikipedia.org/wiki/SAM_(file_format))) files are usually a lot larger and contain all the sequencing data aligned to our genome reference. [Fasta](https://en.wikipedia.org/wiki/FASTA_format) files (not really short for anything) are the simplest of all; they only contain sequences and descriptions of the sequences.

## Background

[Official File Format Specifications](http://samtools.github.io/hts-specs/). Includes VCF,  SAM, CRAM, BAM, BCF, CSI, Tabix, crypt4gh, htsget, and Refget

[What VCF data looks like]()
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

[What SAM data looks like]()
```
@HD VN:1.6 SO:coordinate
@SQ SN:ref LN:45
r001
r002
r003
r004
r003
r001
99ref7 0ref9 0ref9 0ref16
2064 ref 29
 147 ref 37
30 8M2I4M1D3M =37 30 3S6M1P1I4M *0 30 5S6M *0 30 6M14N5M *0 17 6H5M *0 30 9M =7
 39 TTAGATAAAGGATACTG *
  0 AAAAGATAAGGATA    *
  0 GCCTAAGCTAA       *
  0 ATAGCTTCAGC       *
  0 TAGGC             *
-39 CAGCGGCAT         *
SA:Z:ref,29,-,6H5M,17,0;
SA:Z:ref,9,+,5S6M,30,1;
NM:i:1
```

BAM data is the same as SAM only compressed and in binary form. When converted, it looks just like SAM data. Raw, it looks like this (using `hexdump`):
```
0000000 42 41 4d 01 00 00 00 00 18 00 00 00 05 00 00 00
0000010 63 68 72 31 00 3d 43 db 0e 05 00 00 00 63 68 72
0000020 32 00 8d ed 7e 0e 05 00 00 00 63 68 72 33 00 1e
0000030 95 cd 0b 05 00 00 00 63 68 72 34 00 64 c8 64 0b
0000040 05 00 00 00 63 68 72 35 00 3c 8c c8 0a 05 00 00
0000050 00 63 68 72 36 00 3b 02 33 0a 05 00 00 00 63 68
0000060 72 37 00 67 43 7c 09 05 00 00 00 63 68 72 38 00
0000070 76 56 b9 08 05 00 00 00 63 68 72 39 00 f7 be 6a
0000080 08 06 00 00 00 63 68 72 31 30 00 9b 18 14 08 06
0000090 00 00 00 63 68 72 31 31 00 34 09 0c 08 06 00 00
```


