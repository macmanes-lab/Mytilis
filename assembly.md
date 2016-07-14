```
Trinity --seqType fq --JM 150G --SS_lib_type FR \
--left mytilus.muscle.lighter25.trimP2_1P.fastq,mytilus.gill.lighter25.trimP2_1P.fastq  \
--right mytilus.muscle.lighter25.trimP2_2P.fastq,mytilus.gill.lighter25.trimP2_2P.fastq \
--CPU 20 --output MG.lighter.P2 --group_pairs_distance 999 --inchworm_cpu 10 --bflyHeapSpaceMax 50G
```

```
BinPacker -d -q -s fq -p pair \
-l <(cat mytilus.muscle.lighter25.trimP2_1P.fastq mytilus.gill.lighter25.trimP2_1P.fastq) \
-r <(mytilus.muscle.lighter25.trimP2_2P.fastq mytilus.gill.lighter25.trimP2_2P.fastq) -m RF -k 25 -g 200 -o myt_binpacker
```
