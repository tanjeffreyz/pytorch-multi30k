<h1 align="center">PyTorch Multi30k</h1>

Patch for PyTorch's Multi30k machine translation dataset (WMT16). 
As of August 16, 2023, `torchtext.datasets.Multi30k` tries to retrieve data from http://www.quest.dcs.shef.ac.uk/wmt16_files_mmt, which is still unreachable.

To fix this, add these lines before using the `Multi30k` dataset:
```
from torchtext.datasets import multi30k, Multi30k

multi30k.URL['train'] = 'https://raw.githubusercontent.com/tanjeffreyz/pytorch-multi30k/main/training.tar.gz'
multi30k.URL['valid'] = 'https://raw.githubusercontent.com/tanjeffreyz/pytorch-multi30k/main/validation.tar.gz'
multi30k.URL['test'] = 'https://raw.githubusercontent.com/tanjeffreyz/pytorch-multi30k/main/mmt16_task1_test.tar.gz'
multi30k.MD5['test'] = 'd914ec964e2c5f0534e5cdd3926cd2fe628d591dad9423c3ae953d93efdb27a6'
```

**Disclaimer: All rights belong to the authors of the original dataset under the original license.**
