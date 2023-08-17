<h1 align="center">PyTorch Multi30k</h1>

Patch for PyTorch's Multi30k machine translation dataset (WMT16). 
As of August 16, 2023, `torchtext.datasets.multi30k` tries to retrieve data from http://www.quest.dcs.shef.ac.uk/wmt16_files_mmt, which is still unreachable.

To fix this, add these lines before using the `Multi30k` dataset:
```




```

