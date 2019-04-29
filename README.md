# CoInCo Usim data

## Description

This repository contains a file with sentence pairs extracted from the Concepts in Context (CoInCo) corpus (Kremer et al., 2014), a subset of the MASC corpus (Ide et al., 2008) where all content words in sentences were manually annotated with substitutes. 

We paired all instances of a target word that had at least 4 substitutes and kept pairs with (1) no overlap in substitutes (DIFF), and (2) an overlap of at least 75% (SAME).
We treat DIFF as examples of very distinct usages of a word, and SAME as examples where the word is used with the same meaning.
This is the dataset used in the paper Garí Soler et al., (2019) after balancing the classes.

If you use this dataset, please cite the paper:
```
@inproceedings{gari2019word,
  title={Word Usage Similarity Estimation with Sentence Representations and Automatic Substitutes},
  author={Gar\'i Soler, Aina and Apidianaki, Marianna and Allauzen, Alexandre},
  booktitle={{Proceedings of the Eighth Joint Conference on Lexical and Computational Semantics, Minneapolis, MN}},
  year={2019},
  organization={Association for Computational Linguistics}
}
```

The CoInCo corpus can be found [here](https://www.ims.uni-stuttgart.de/forschung/ressourcen/korpora/coinco.html),
under the CC-BY-3.0-US license.

## Format 

In coinco_usim_data.csv each line is a sentence pair:
- id: <id of sentence 1>-<id of sentence 2>-cnc
- lemma_pos: lemma and part-of-speech of the target word
- score: 1 for DIFF, 5 for SAME.
- word1: word as it appears in the first sentence of the pair
- position1: position of the word in the first sentence starting from 0, with given tokenization
- sentence1: tokenized first sentence of the pair
(analogously for word2, position2, sentence2).

The file train_cnc_ids.txt contains the ids used as training data in the original paper, one per line.

## References

Aina Garí Soler, Marianna Apidianaki, and Alexandre Allauzen. 2019. Word Usage Similarity Estimation with Sentence Representations and Automatic Substitutes. In Proceedings of the Eighth Joint Conference on Lexical and Computational Semantics, Minneapolis, MN. Association for Computational Linguistics.

Gerhard Kremer, Katrin Erk, Sebastian Pado, Stefan Thater. 2014. [What Substitutes Tell Us – Analysis of an “All-Words” Lexical Substitution Corpus.](http://www.aclweb.org/anthology/E14-1057.pdf) In Proceedings of the 14th Conference of the European Chapter of the Association for Computational Linguistics. pages 540-549, Göteborg, Sweden. Association for Computational Linguistics.

Nancy Ide, Collin Baker, Christiane Fellbaum, Charles Fillmore, and Rebecca Passonneau. 2008. [MASC: The Manually Annotated Sub-Corpus of American English.](http://www.lrec-conf.org/proceedings/lrec2008/pdf/617_paper.pdf) In Proceedings of the Sixth International Conferences on Language Resources and Evaluation. Marrakech, Morocco. European Language Resources Association. 


