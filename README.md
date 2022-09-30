MLExample
=========

Andrew C.R. Martin, UCL 2022
----------------------------

This serves as a set of simple examples for using Weka for machine learning
and our own `csv2arff` program for creating the datafiles for Weka.

Read the **Installation** instructions below for setting up Weka and `csv2arff`

The examples are in subdirectories:

- `example1` is an example using a single BASH script with a balanced dataset
- `example2` is....


Installation
------------

### 1. Install a Java runtime if you don't have one already

Under Fedora/CentOS/RHEL/etc.: `yum -y install java`

### 2. Install Weka

Download the Weka software from https://www.cs.waikato.ac.nz/ml/weka/

Follow the instructions for installation. If you are running under
Linux, then unpack the ZIP file in your home directory. e.g.
```
cd
unzip weka-3-8-6-azul-zulu-linux.zip
```
This will create a directory called (for example) `weka-3-8-6`. Now
create a symbolic link (shortcut in Windows-speak) that is just called
`weka`. For example:
```
cd
ln -s weka-3-8-6 weka
```

### 3. Put `csv2arff` into your path

*These instructions are for the BASH shell under Linux, Mac or git-bash
(Windows)*

A version of `csv2arff` is provided here, but the latest version will
always be in https://github.com/AndrewCRMartin/bioscripts/

First of all, create a `~/bin` directory if it doesn't exist and copy the
script there if it doesn't exist already:
```
mkdir -p ~/bin
if [ ! -e ~/bin/csv2arff ]; then cp csv2arff/csv2arff.pl ~/bin/csv2arff; fi
```

Now ensure that `~/bin` is in your path:
```
if [ X`echo $PATH | grep ${HOME}/bin` != "X" ]; then echo "It's there"; else echo "You need to add ${HOME}/bin to your path"; fi
```

If this tells you that you need to add the bin directory to your path
then you need to edit `~/.bashrc` and add the line: 
```
export PATH="$PATH:$HOME/bin"
```
at the end of the file. Once you have saved the file, at the command prompt, type:
```
source ~/.bashrc
```





