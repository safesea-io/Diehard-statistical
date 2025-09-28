<img src="logo.png" alt="logo" width="200"/>

# Statistical test 

SafeSea is a company specialized in providing entropy base on natural forces ( the sea ) Random Number Generation, or RNG, is a key component to applications that benefit from true randomness. 

This is result of Dieharder statistical test suite for Random Number Generator (RNG) that apply to safeSea generated RNG List    

# Diehard Statistical Test Suite
  
> Diehard tests are a battery of statistical tests for measuring the quality of a random
number generator. It contains 16 statistical tests. This battery was developed by George
Marsaglia over several years and first published in 1995. It is a complete, thorough and
comprehensive set of statistical tests for PRNG. This set of statistical tests serves as
some kind of litmus for checking and eventual certification of PRNG. If a PRNG
passes Diehard statistical tests, then it can be used in more serious scientific researches.

[Dieharder Statistical Test Suite](https://webhome.phy.duke.edu/~rgb/General/dieharder.php)

### Installation
- You can install dieharder test suite directly from Linux Package Managesment. 
(Ubuntu)
```sh
$ sudo apt-get install dieharder
```

Get the sample of random number that we provide on github ( 76.936.939 random numbers with 16bit ) .
- Clone the repository or just download zip file and all extended file (FromSea.dataset.tar.gz.*).
- unzip the file and you will get FromSea_dataset.txt (the random-number-file gotten from the SafeSea Engine).
```sh
$ cat FromSea.dataset.tar.gz.* | tar xzvf -
```


### Run the test
```sh
$ dieharder -g 202 -f FromSea_dataset.txt [-D default -D histogram]
```

### Output and visualization

You can read the result in output2.txt on github or read output of the test suite when you run the command above.

Sample of `result`:

```
#=============================================================================#
#            dieharder version 3.31.1 Copyright 2003 Robert G. Brown          #
#=============================================================================#
   rng_name    |           filename             |rands/second|
     file_input|                FromSea_out2.txt|  2.47e+06  |
#=============================================================================#
        test_name   |ntup| tsamples |psamples|  p-value |Assessment
#=============================================================================#
   diehard_birthdays|   0|       100|     100|0.54063476|  PASSED
```
