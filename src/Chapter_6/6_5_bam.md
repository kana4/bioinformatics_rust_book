# Bam File Format

BAM data is the same as SAM only compressed and in binary form. BAM is kind of like the `.zip` file version of a plaintext SAM, so we don't need to deal with BAMs directly unless we really know what we're doing. When converted, it looks just like SAM data, which is plaintext. Raw, it looks like this (using `hexdump file.bam`):

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

Ok, so this isn't binary. Just like the command specifies, this is the [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) representation of our binary data, which is (paraphrasing from Wikipedia) easier to read (but is it really...) Also paraphrasing from wikipedia:

    Each hexadecimal digit represents four bits (binary digits), also known as a nibble (or nybble), which is 1/2 of a byte. For example, a single byte can have values ranging from 00000000 to 11111111 in binary form, which can be conveniently represented as 00 to FF in hexadecimal.

Again, we don't have to deal with BAM directly, similarly to how we don't deal with `.zip` files directly, we `unzip` them, probably with [samtools](http://www.htslib.org)

[Official File Format Specifications](http://samtools.github.io/hts-specs/). Includes VCF, SAM, CRAM, BAM, BCF, CSI, Tabix, crypt4gh, htsget, and Refget
