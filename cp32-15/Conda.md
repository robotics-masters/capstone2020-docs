# Conda #
## Tips and Tricks ##

### Pip with Conda ###
As far as a I can tell, the simple rules are:

* Try to install something new with conda first using `conda install` (`conda search` is helpful for finding packages and their versions).
* If you pip install something, it will install it to your currently activated conda environment.
* There are limits to compatiblity between pip and conda. Conda "tries" to be as compatible with pip as possible, but this fails sometimes.

### Save a Backup of an Environment ###
For example, create a backup of the donkey environment:
```
conda create --name donkey-backup --clone donkey
```

### List environments ###
```
conda env list
```

### Delete environment ###
```
conda env remove --name myenv
```