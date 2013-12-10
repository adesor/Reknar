Reknar
======

Reknar is a python based web page ranker. It uses a basic version of PageRank.
Compatible with Python 2.7.X

To use:
```Python
>>> from reknar import Reknar
>>> reknar = Reknar(graph) # graph can be any URL graph of the form {URL1 : [outlink1, outlink2,...], URL2 : [outlink3,...],...}
```

To use with Redips:
```Python
>>> from reknar import Reknar
>>> import redips
>>> red = redips.load('redips-pickle-file')
>>> reknar = Reknar(red.get_graph())
```

The initializer takes an optional pickle file argument ('reknar.pickle' by default)
```Python
>>> reknar = Reknar(graph, 'my_pickle_file.pickle')
```

To compute the ranks based on the given graph:
```Python
>>> reknar.compute_ranks()
```

To access the ranks:
```Python
>>> reknar.get_ranks()
```

To update the graph of the Reknar object:
```Python
>>> reknar.update(graph) # graph is the new graph you want to update the Reknar's graph with
```

To save the state of Reknar:
```Python
>>> reknar.save()
```

To load the Reknar object from its pickle:
```Python
>>> from reknar import load
>>> reknar = load('pickle-file.pickle')
```
