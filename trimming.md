```
java -Xmx50g -jar /share/trinityrnaseq-code/trinity-plugins/Trimmomatic-0.32/trimmomatic-0.32.jar PE \
-threads 48 -baseout mytilus.muscle.lighter25.trimP2.fastq \
../corrected/mytilus.muscle.1.fq.cor.fq.gz \
../corrected/mytilus.muscle.2.fq.cor.fq.gz  \
ILLUMINACLIP:/share/trinityrnaseq-code/trinity-plugins/Trimmomatic-0.32/adapters/TruSeq3-PE.fa:2:30:10 \
SLIDINGWINDOW:4:2 \
LEADING:2 \
TRAILING:2 \
MINLEN:25
```

```
java -Xmx50g -jar /share/trinityrnaseq-code/trinity-plugins/Trimmomatic-0.32/trimmomatic-0.32.jar PE \
-threads 48 -baseout mytilus.gill.lighter25.trimP2.fastq \
../corrected/mytilus.gill.1.fq.cor.fq.gz \
../corrected/mytilus.gill.2.fq.cor.fq.gz  \
ILLUMINACLIP:/share/trinityrnaseq-code/trinity-plugins/Trimmomatic-0.32/adapters/TruSeq3-PE.fa:2:30:10 \
SLIDINGWINDOW:4:2 \
LEADING:2 \
TRAILING:2 \
MINLEN:25
```
