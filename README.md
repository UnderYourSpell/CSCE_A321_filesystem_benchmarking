#Running Filebench
https://github.com/filebench
More help is in the README file
### Instructions
Need a Linux OS
Need to install yacc and lex
you can use the command:
```
sudo apt-get install bison flex
```
Then download the zip file for Filebench from:
https://github.com/filebench/filebench/releases

Navigate to the file in Terminal
Then with yacc and lex installed, run:
```
$ ./configure
$ make
$ sudo make install
```

Next you need to turn off ASLR (Address Space Layout Randomization):
```
echo 0 | sudo tee /proc/sys/kernel/randomize_va_space
```
A 0 is printed if successful

Now to run a workload, you can either run one from the predefined workloads in the workloads folder in the Filebench folder
It can be done with this command
```
sudo filebench -f yourworkload.f
```
If all goes well the results should be printed

More info on filebench at:
https://www.usenix.org/system/files/login/articles/login_spring16_02_tarasov.pdf 