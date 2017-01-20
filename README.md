[![DOI](https://zenodo.org/badge/22548/SELAB-AA/fragbinpacking-results.svg)](https://zenodo.org/badge/latestdoi/22548/SELAB-AA/fragbinpacking-results)
# fragbinpacking-results
Results for the Fragmentable Items Bin Packing Problem

b3_time.tsv is a tab-separated value file.
Each row corresponds to one problem instance.
Column M contains the number of bins before reduction by E1 E2.
Column M' contains the number of bins after reduction by E1 E2.
Column N contains the number of items before reduction by E1 E2.
Column N' contains the number of items after reduction by E1 E2.
Column W contains the number of unique item sizes after reduction by E1 E2.
Column T contains the number of seconds required to run B3.

The results from the experiment are contained in a compressed zip archive.
A pair of files is associated with each run of each problem instance:
uniform_{capacity}_{low}_{high}_{items}_{problem}_{run}.dat
uniform_{capacity}_{low}_{high}_{items}_{problem}_{run}.gen

{capacity} is the bin capacity,
{low} and {high} are the range of item sizes and {items} is the number of items.
{problem} is the problem identifier within the problem class and {run} is the run.

The dat file contains information about the solution and problem instance.
The first line indentifies the seed of the random number generator used.
The second line gives the number of items before reduction by E1 E2.
The second line gives the number of items after reduction by E1 E2.
The fourth line tells how many seconds it took to perform the reduction.
The fifth line gives the number of bins after reduction.
The sixth line presents the lower bound expressed as the minimum number of cuts.
The seventh line presents the upper bound expressed as the maximum number of cuts.
Lines 8--9 give the format of the actual data, which is a space-separated list
of the number of block in the best solution, the corresponding number of cuts and the
number of seconds it took to run.

Lines 10--14 express the order of the data. First comes the results from only
using algorithm G once on the reduced input. Then we have the results
from running algorithm B3 G^+ once on the reduced input. Thereafter come the results
after creating the intitial population for the grouping genetic algorithm. This
amounts to the best solution after creating NP = 100 individuals using B3G^+.
The final line presents the results after running the rest of the genetic algorithm.

The gen file contains a list of the number of blocks in the best solution of the
population for each generation of the grouping genetic algorithm, including generation 0.

