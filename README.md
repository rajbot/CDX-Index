CDX-Index
=========

Tools for merging sorted, compressed CDX files and producing IDX index files

```bash
#Merge compressed sorted cdx files:
$ wayback-cdx-idx-merge.py [options] cdx1 cdx2 ..   

#Merge using file list
$ wayback-cdx-idx-merge.py [options] - < file-list.txt

#Can do sharded subset, outputting compressed data and index file:
$ wayback-cdx-idx-merge.py [options] --total-shards N --do-shard M --idx=out.idx --idx-filefield=something cdx1 idx1 cdx2 idx2 ... 

# Explicitly cache shard cutpoints:
$ wayback-cdx-idx-merge.py --generate-cutpoints-file file --total-shards N cdx1 idx1 cdx2 idx2 ...

# Compress and output index data for a single cdx stream:
$ wayback-cdx-idx-merge.py [options] --zipnum-mode --idx=out.idx --idx-filefield=something < data > out.gz
