# The AMI Meeting Parallel Corpus
©2020, The University of Tokyo

# Corpus Description

The [original AMI Meeting Corpus](http://groups.inf.ed.ac.uk/ami/corpus/index.shtml) is a multi-modal dataset containing 100 hours of meeting recordings in English.
The parallel version was constructed by asking professional translators to translate utterances from the original corpus into Japanese. Since the original corpus consists of speech transcripts, the English sentences contain a lot of short utterances (e.g., "Yeah", "Okay") or fillers (e.g., "Um"), and these are translated into Japanese as well. Therefore, it contains many duplicate sentences.

We provide training, development and evaluation splits from the AMI Meeting Parallel Corpus. In this repository we publicly share the full development and evaluation sets and a part of the training data set.

|        	| Training 	| Development 	| Evaluation 	|
|--------	|---------:	|:-----------:	|:----------:	|
| Sentences |   20,000 	|       2,000 	|      2,000 	|
| Scenarios |   30 	|       5	 	|      5	 	|


# Corpus Structure

The corpus is structured in json format consisting of documents, which consist of sentence pairs. Each sentence pair has a sentence number, speaker identifier (to distinguish different speakers), text in English and Japanese, and original language (always English).

```json
[
		{
			"id": "IS1004a",
			"original_language": "en",
			"conversation": [
				...,
				{
					"no": 22,
					"speaker": "A",
					"ja_sentence": "では、このプロジェクトの目的は、あー、新しいリモコンを作ることです。",
					"en_sentence": "So, the goal of this project is to uh developed a new remote control."
				},
				...
			]
		},
		...
]
```

## License
Our dataset is released under the [Creative Commons Attribution-ShareAlike (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/legalcode).

## Reference
If you use this dataset, please cite the following paper:
Matīss Rikters, Ryokan Ri, Tong Li, and Toshiaki Nakazawa (2020). "[Document-aligned Japanese-English Conversation Parallel Corpus](http://www.statmt.org/wmt20/pdf/2020.wmt-1.74.pdf)." In Proceedings of the Fifth Conference on Machine Translation, 2020.
```bibtex
@InProceedings{rikters-EtAl:2020:WMT,
  author    = {Rikters, Matīss  and  Ri, Ryokan  and  Li, Tong  and  Nakazawa, Toshiaki},
  title     = {Document-aligned Japanese-English Conversation Parallel Corpus},
  booktitle      = {Proceedings of the Fifth Conference on Machine Translation},
  month          = {November},
  year           = {2020},
  address        = {Online},
  publisher      = {Association for Computational Linguistics},
  pages     = {637--643},
  url       = {https://www.aclweb.org/anthology/2020.wmt-1.74}
}
```

## Acknowledgements
This work was supported by "Research and Development of Deep Learning Technology for Advanced Multilingual Speech Translation", the Commissioned Research of National Institute of Information and Communications Technology (NICT), JAPAN.
