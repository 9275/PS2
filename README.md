# PS2

Compile using:
```
g++ -DSIGSPAN -std=c++11 -O3 -o experiments/algorithms/p *.cpp
```
to include sigspan support (needed for the experiments). The -DSIGSPAN flag can be omitted when this is not needed. Simply running the command with no flags or input files will display the possible flags and options:
```
./p [options] <data> <patterns>
output options:
 -o <filename> output result to file instead of stdio
 -v Verbose
 -V Extra verbose
Pattern Statistics:
 -s Output support
 -c Output number of sequences with non-zero probability
PS² options:
 -e Output expected value
 -d Output standard deviation
 -p Output p-value (exact)
 -P Output -log(p-value) (exact)
 -n Output p-value (normal approximation)
 -N Output -log(p-value) (normal approximation)
 -l Output p-value (Poisson approximation)
 -L Output -log(p-value) (Poisson approximation)
Significance options:
 -B <alpha> Bonferroni significance threshold
 -W <alpha> Westfall-Young significance threshold (PS²)
SigSpan options:
 -b Output expected value
 -i Output p-value
 -I Output -log(p-value)
```

# Experiments
Experiments are scripts created in python 3. These can be run by simply invoking the commands:
```
cd experiments/
./run_real_data.py
./run_artificial_data.py
./run_artificial_data_MultiDist.py
```
Ensure that all libraries contained in experiments/requirements.txt are present in the python installation. This can be done using a command such as:
```
pip3 install -r requirements.txt
```
