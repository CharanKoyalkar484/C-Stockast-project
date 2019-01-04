# Stockast [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FRajdeepKonwar%2Fstockast.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FRajdeepKonwar%2Fstockast?ref=badge_shield)
## Stock Market Forecasting using Parallel (OpenMP) Monte-Carlo Simulations

### Compile Instructions
#### Windows
* Open stockast.sln
* Right-click Solution 'stockast' in the Solution Explorer and select `Retarget solution`
* Build and run!

#### Linux
##### **Local machine**
```
make
```
Type `make clean` to clean object file and executable.
##### **Remote machine**
```
g++ stockast.cpp -o stockast -fopenmp
```

### Run Instructions
#### Windows
Simply run from Visual Studio or double-click the executable created inside x64\\{config}\stockast.exe

#### Linux
Set the number of threads to be used for computation,
```
export OMP_NUM_THREADS=number_of_threads
```
For example, `export OMP_NUM_THREADS=8`.
Then run the program
```
./stockast
```

### General info
* The input file "ml_data.csv" contains the stock-price values for the 3 hours.
* The output file "opt.csv" contains the output (most likely outcome) price-vector from our code. One can use Excel or gnuplot to plot the resulting line graph of the predicted stock pricing.
* (**Linux only**) The script "profiling.sh" runs the parallel code from 1 to the maximum number of threads in your system. To use the script,
```
./profiling.sh "number_of_threads"
```
For example, `./profiling.sh 8`.
