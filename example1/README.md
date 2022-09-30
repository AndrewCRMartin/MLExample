Example 1
=========

This is a simple example using a balanced dataset. It doesn't do any
cross-validation but simply splits the data into a training set and a
test set.


Run the example by typing:
```
./demo.sh
```

The code creates a dataset by taking a CSV file containing
features. Since we know the size of this file (61203 data points) and
the data are in random order, the script pulls out the first 50000
data points for the training data and the remainder as a test set.

The data are the converted from a CSV file into an ARFF file using
`csv2arff`. This reads the file `inputs.dat` which specifies which
columns from the CSV file are to be used as inputs and takes the name
of the output column on the command line. It also skips any records
with missing data.

Next the script trains a Random Forest in Weka using 100 trees. At the
end of the training, the file `test.arff` contains the trained model
and `test.out` contains the performance *on the training data* (which
will be very close to perfect) and using built-in cross-validation.

Finally the script tests the performance of the saved model using the
test set that we kept back at the start. Results for that are present
in `test2.out`.

