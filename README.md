# DNA Calculations in python

>NAME: Emily Friedman
>DATE: 2025-02-24

--------------------------------
Extract the 20th sequence from `Bjimenezi_Churi2.fq`:

```bash
head -100 Bjimenezi_Churi2.fq | sed -n '2~4p' | sed -n '20p' > churi2_seq20.txt
cat churi2_seq20.txt
	CATGCTGGGAGTTGTAGTTTCTCAACAGCTGGAGAGCCGCAGGTTTGAGACCCATGGTCTATACAGACAATACAGGAAGAAAGTTTGTGTCTCCAATATGGCTGCTCCAGGGAAGTTTAT
```

dnacalc.py

```python
#!/usr/bin/python3
file = open("data/churi2_seq20.txt", "r")
dnaseq = file.read()
print ('Sequence:', dnaseq)

seq_length = len(dnaseq)
print ('Sequence Length:', seq_length)

A_count = dnaseq.count('A')
C_count = dnaseq.count('C')
G_count = dnaseq.count('G')
T_count = dnaseq.count('T')

print ("Base Percentages:")
print ("A: %.1f" % (100 * A_count/seq_length))
print ("C: %.1f" % (100 * C_count/seq_length))
print ("G: %.1f" % (100 * G_count/seq_length))
print ("T: %.1f" % (100 * T_count/seq_length))
```

Output:

```bash
Sequence: CATGCTGGGAGTTGTAGTTTCTCAACAGCTGGAGAGCCGCAGGTTTGAGACCCATGGTCTATACAGACAATACAGGAAGAAAGTTTGTGTCTCCAATATGGCTGCTCCAGGGAAGTTTAT

Sequence Length: 121

Base Percentages:
A: 26.4
C: 19.0
G: 27.3
T: 26.4
```

--------------------------------------------------
Enjoy my favorite figure I've ever made :)

![](https://github.com/efriedman2/new-repo/blob/main/files/phnpc_umap.jpg)

