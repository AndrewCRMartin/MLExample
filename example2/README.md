Example 2
=========

This is a slightly more complex example where we do balancing of the
dataset using `csv2arff`. The dataset has ~2200 examples in the `pd`
class and ~1100 examples in the `snp` class.

The `doit_prepare` script generates 3 ARFF files each containing ~1100
`snp` entries and ~1100 `pd` entries selected randomly.

Run it by typing:
```
./doit_prepare
```

The `doit_learn` script runs through each of the `.arff` files created
by `doit_prepare` and creates filenames for the trained model and
output. It then runs the training for each `.arff` file in turn. This
includes cross-validation done within the Weka code. Finally it
extracts the cross-validated performance metrics from the output files
and displays them.

Run it by typing:
```
./doit_learn
```


