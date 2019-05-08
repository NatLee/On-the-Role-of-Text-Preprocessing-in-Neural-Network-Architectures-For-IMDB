
#  On the Role of Text Preprocessing in Neural Network Architectures

### An Evaluation Study on Text Categorization and Sentiment Analysis

Jose Camacho Collados and Mohammad Taher Pilehvar


### Information

This is **UNOFFICIAL** code for this [paper](https://arxiv.org/abs/1707.01780) and only run with IMDb dataset.
These files are modified from original code [sensecnn](https://github.com/pilehvar/sensecnn) for compatibility on Python3 and research.

### Pre-trained word embeddings

You can find them from the original authors [HERE](https://github.com/pedrada88/preproc-textclassification/blob/master/README.md).

### Usage

This repository has already included [IMDb dataset](https://ai.stanford.edu/~amaas/data/sentiment/).
If you use it, please cite the original source.


Please use commandline with following steps.

```bash
python prepare_dataset.py
```

If you have not downloaded pre-trained word embeddings, just run.
```bash
python __main__.py IMDb data
```

Run with pre-trained embeddings.
```
python __main__.py IMDb data --emb=<YOUR_PRE_TRAIN_WORD2VEC_PATH>
```

The default settings about training in `__main__.py` are shown as following.

```python
settings = { 'dict':'data/'+self.dataset+'/'+ self.dataset_id + '.dict.pkl',
                     'data':'data/'+self.dataset+'/'+ self.dataset_id +'.pkl',
                     'filter_length':2,
                     'pool_length':2,
                     'nb_filter':50,
                     'lstm_output_size':25,
                     'batch_size':100,
                     'nb_epoch':100,
                     'folds':10
                    }
```


### Reference paper

If you use any of these resources, please cite the original papers:
```
@InProceedings{camacho:preprocessing2018,
  author = 	"Camacho-Collados, Jose and Pilehvar, Mohammad Taher",
  title = 	"On the Role of Text Preprocessing in Neural Network Architectures: An Evaluation Study on Text Categorization and Sentiment Analysis",
  booktitle = 	"Proceedings of the EMNLP Workshop on Analyzing and interpreting neural networks for NLP",
  year = 	"2018",
  publisher = 	"Association for Computational Linguistics",
  location = 	"Brussels, Belgium"
}


@InProceedings{pilehvar-EtAl:2017:Long,
  author    = {Pilehvar, Mohammad Taher  and  Camacho-Collados, Jose  and  Navigli, Roberto  and  Collier, Nigel},
  title     = {Towards a Seamless Integration of Word Senses into Downstream NLP Applications},
  booktitle = {Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)},
  month     = {July},
  year      = {2017},
  address   = {Vancouver, Canada},
  publisher = {Association for Computational Linguistics},
  pages     = {1857--1869},
  url       = {http://aclweb.org/anthology/P17-1170}
}
```


