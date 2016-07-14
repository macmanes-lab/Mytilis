```
kallisto index -i transcripts2.idx ../assembly/Mytilus.MG.fasta
kallisto quant -t 32 -i transcripts2.idx -o kallisto_muscle2 -b 100 \
/mnt/reads/mytilus.muscle.lighter25.trimP2_1P.fastq.gz \
/mnt/reads/mytilus.muscle.lighter25.trimP2_2P.fastq.gz

kallisto quant -t 32 -i transcripts2.idx -o kallisto_gill2 -b 100 \
/mnt/reads/mytilus.gill.lighter25.trimP2_1P.fastq.gz \
/mnt/reads/mytilus.gill.lighter25.trimP2_2P.fastq.gz

salmon index -t ../assembly/Mytilus.MG.fasta -i transcripts2_index --type quasi -k 31
~/salmon-0.5.1/bin/salmon quant -p 32 -i transcripts2_index -l MSR \
-1 <(gzip -cd /mnt/reads/mytilus.gill.lighter25.trimP2_1P.fastq.gz) \
-2 <(gzip -cd /mnt/reads/mytilus.gill.lighter25.trimP2_2P.fastq.gz) -o salmon_gill2

salmon quant -p 32 -i transcripts2_index -l MSR \
-1 <(gzip -cd /mnt/reads/mytilus.muscle.lighter25.trimP2_1P.fastq.gz) \
-2 <(gzip -cd /mnt/reads/mytilus.muscle.lighter25.trimP2_2P.fastq.gz) -o salmon_muscle2
```
