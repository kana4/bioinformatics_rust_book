# VCF File Format

First, a quick look at what VCF data looks like (description at the bottom of this page):

```
##fileformat=VCFv4.0
##fileDate=20100610 
##source=glfTools v3
##reference=1000GenomesPilot-NCBI36 
##phasing=NA
##INFO=<ID=NS,Number=1,Type=Integer,Description="Number of Samples With Mapped Reads">
##INFO=<ID=DP,Number=1,Type=Integer,Description="Total Depth">
##INFO=<ID=DB,Number=0,Type=Flag,Description="dbSNP membership, build 129">
##INFO=<ID=H2,Number=0,Type=Flag,Description="HapMap2 membership">
##FILTER=<ID=NUYR,Description="Variant in non-unique Y region">
(base) l@mbp Downloads % head -100 test.vcf
##fileformat=VCFv4.0
##fileDate=20100610 
##source=glfTools v3
##reference=1000GenomesPilot-NCBI36 
##phasing=NA
##INFO=<ID=NS,Number=1,Type=Integer,Description="Number of Samples With Mapped Reads">
##INFO=<ID=DP,Number=1,Type=Integer,Description="Total Depth">
##INFO=<ID=DB,Number=0,Type=Flag,Description="dbSNP membership, build 129">
##INFO=<ID=H2,Number=0,Type=Flag,Description="HapMap2 membership">
##FILTER=<ID=NUYR,Description="Variant in non-unique Y region">
##FORMAT=<ID=GT,Number=1,Type=String,Description="Genotype">
##FORMAT=<ID=GQ,Number=1,Type=Integer,Description="Genotype	Quality">
##FORMAT=<ID=DP,Number=1,Type=Integer,Description="Depth">
##INFO=<ID=AC,Number=.,Type=Integer,Description="Allele count in genotypes">
##INFO=<ID=AN,Number=1,Type=Integer,Description="Total number of alleles in called genotypes">
#CHROM	POS	ID	REF	ALT	QUAL	FILTER	INFO
Y	2728456	rs2058276	T	C	32	.	AC=2;AN=2;DB;DP=182;H2;NS=65
Y	2734240	.	G	A	31	.	AC=1;AN=2;DP=196;NS=63
Y	2743242	.	C	T	25	.	AC=1;AN=2;DP=275;NS=66
Y	2746727	.	A	G	34	.	AC=2;AN=2;DP=179;NS=64
Y	2777970	.	T	A	67	.	AC=1;AN=2;DP=225;NS=67
Y	2782506	rs2075640	A	G	38	.	AC=1;AN=2;DB;DP=254;H2;NS=66
Y	2783755	.	G	A	51	.	AC=1;AN=2;DP=217;NS=67
Y	2788927	rs56004558	A	G	38	.	AC=1;AN=2;DB;DP=173;NS=60
Y	2813908	.	T	G	46	.	AC=1;AN=2;DP=188;NS=67
Y	2815679	.	T	C	30	.	AC=1;AN=2;DP=205;NS=64
Y	2816471	rs9785784	T	A	40	.	AC=1;AN=2;DB;DP=212;NS=64
Y	2841844	.	T	G	41	.	AC=1;AN=2;DP=176;NS=56
Y	2891375	.	T	C	29	.	AC=1;AN=2;DP=176;NS=61
Y	2899051	.	C	T	51	.	AC=1;AN=2;DP=206;NS=68
Y	2900301	.	G	A	54	.	AC=1;AN=2;DP=167;NS=65
Y	2923665	rs7892924	G	A	34	.	AC=1;AN=2;DB;DP=171;NS=63
Y	2944029	.	T	C	35	.	AC=1;AN=2;DP=244;NS=61
Y	2947824	rs9786184	A	C	39	.	AC=2;AN=2;DB;DP=206;NS=63
Y	2962839	rs9786562	C	T	33	.	AC=2;AN=2;DB;DP=185;NS=63
Y	2972385	rs9786491	C	T	29	.	AC=1;AN=2;DB;DP=160;NS=55
Y	3034782	.	A	C	40	.	AC=1;AN=2;DP=163;NS=64
Y	3094725	.	C	G	18	.	AC=1;AN=2;DP=179;NS=63
Y	3134753	.	A	T	42	.	AC=1;AN=2;DP=189;NS=65
Y	3144401	.	G	A	46	.	AC=1;AN=2;DP=169;NS=59
Y	3168773	.	C	T	43	.	AC=1;AN=2;DP=173;NS=64
Y	3537173	rs7067327	G	C	31	.	AC=2;AN=2;DB;DP=193;NS=64
Y	3751769	.	A	G	26	.	AC=1;AN=2;DP=173;NS=61
Y	3781790	.	T	A	55	.	AC=1;AN=2;DP=165;NS=59
Y	4176203	.	G	A	18	.	AC=1;AN=2;DP=166;NS=69
Y	4177733	.	A	G	40	.	AC=1;AN=2;DP=177;NS=61
Y	4305332	.	T	C	46	.	AC=1;AN=2;DP=174;NS=69

```

Even if we don't know about the file type, we can start to get an idea that the file has a header followed by a table-looking structure of the actual data. In VCF, each line in a header is denoted by `##`, whereas the column names are denoted by a single `#`. To summarize each column in the data:

<ul>Chromosome: Which chromosome is the alteration on?</ul>
<ul>Position: What position on the chromosome is the alteration on?</ul>
<ul>ID: If this is a well known alteration, what's the ID?</ul>
<ul>Ref: What's the base in the genome reference?</ul>
<ul>Alt: What's the base altered to?</ul>
<ul>Quality: What's the quality related to the alteration or in a not-correct not-incorrect answer, how sure are we of the alteration?</ul>
<ul>Filter: Does the alteration pass a cutoff for quality, or in a not-correct not-incorrect answer, are we more sure or unsure of the alteration?</ul>
<ul>Info: Other information that we couldn't fit into the other columns</ul>