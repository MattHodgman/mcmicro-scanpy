# mcmicro-scanpy
An MCMICRO module implementation of scanpy for clustering cells using the Leiden algorithm.

## Output Files
- `cells.csv` contains the cluster assignment for each cell
- `clusters.csv` contains each clusters' mean values for every feature 
(if the max feature value is >1000 then the values will be log transformed for clustering and remain transformed in this output file)

## Paramenter Reference
```
usage: cluster.py [-h] -i INPUT [-o OUTPUT] [-m MARKERS] [-k NEIGHBORS] [-c]

Cluster cell types using mcmicro marker expression data.

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        Input CSV of mcmicro marker expression data for cells
  -o OUTPUT, --output OUTPUT
                        The directory to which output files will be saved
  -m MARKERS, --markers MARKERS
                        A text file with a marker on each line to specify which markers to use for clustering
  -k NEIGHBORS, --neighbors NEIGHBORS
                        the number of nearest neighbors to use when clustering. The default is 30.
  -c, --method          Include a column with the method name in the output files.
```
