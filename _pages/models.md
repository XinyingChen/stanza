---
title: Models
keywords: models
permalink: '/models.html'
---

## Models for Human Languages

### Downloading and Using Models

Downloading models for human languages of your interest for use in the StanfordNLP pipeline is as simple as

```python
>>> import stanfordnlp
>>> stanfordnlp.download('ar')    # replace "ar" with the language code or treebank code you need, see below
```

The language code or treebank code can be looked up in the next section. If only the language code is specified, we will download the default models for that language (indicated by <i class="fas fa-check" style="color:#33a02c"></i> in the table), which are the models trained on the largest treebank available in that language. If you really care about the models of a specific treebank, you can also download the corresponding models with the treebank code.

To use the default model for any language, simply build the pipeline as follows

```python
>>> nlp = stanfordnlp.Pipeline(lang="es")    # replace "es" with the language of interest
```

If you are using a non-default treebank for the langauge, make sure to also specify the treebank code, for example

```python
>>> nlp = stanford.Pipeline(lang="it", treebank="it_postwita")
```

### Human Languages Supported by StanfordNLP

Below is a list of all of the (human) languages supported by StanfordNLP (through its neural pipeline). The performance of these systems on the [CoNLL 2018 Shared Task](https://universaldependencies.org/conll18/) official test set (in our unofficial evaluation) can be found [here](performance.md).

**Note**

1. Models marked with <i class="fas fa-exclamation-triangle" style="color:#e31a1c"></i> have significantly low unlabeled attachment score (UAS) when evaluated end-to-end (from tokenization all the way to dependency parsing). Specifically, their UAS is lower than 50% on the CoNLL 2018 Shared Task test set. Any use of these models for serious syntactical analysis is strongly discouraged.
2. <i class="fas fa-flag" style="color:#fdae61"></i> marks models that are at least 1% absolute UAS worse than the full neural pipeline presented in [our paper](https://nlp.stanford.edu/pubs/qi2018universal.pdf) (which uses the [Tensorflow counterparts](https://github.com/tdozat/Parser-v3) for the tagger and the parser), so that might raise a yellow flag.

| Language | Treebank | Language code | Treebank code | Models | Version | Treebank License | Treebank Doc |  Notes |
| :------- | :------- | :------------ | :------------ | :----- | :------ | :--------------: | :-----------: | :---- |
| Afrikaans | AfriBooms | af | af_afribooms | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/af_afribooms_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/af_afribooms/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Ancient Greek | Perseus | grc | grc_perseus | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/grc_perseus_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/2.5/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/2.5/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/grc_perseus/index.html) |  |
|  | PROIEL | grc | grc_proiel | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/grc_proiel_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/grc_proiel/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Arabic | PADT | ar | ar_padt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ar_padt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ar_padt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Armenian | ArmTDP | hy | hy_armtdp | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/hy_armtdp_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/hy_armtdp/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Basque | BDT | eu | eu_bdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/eu_bdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/eu_bdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Bulgarian | BTB | bg | bg_btb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/bg_btb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/bg_btb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Buryat | BDT | bxr | bxr_bdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/bxr_bdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/bxr_bdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-exclamation-triangle" style="color:#e31a1c"></i> |
| Catalan | AnCora | ca | ca_ancora | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ca_ancora_models.zip) | 0.2.0 | <a rel="license" href="https://www.gnu.org/licenses/gpl-3.0.en.html"><img alt="GNU License" style="height:15px; width:auto" src="https://www.gnu.org/graphics/gplv3-88x31.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ca_ancora/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Chinese (traditional) | GSD | zh | zh_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/zh_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/zh_gsd/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Croatian | SET | hr | hr_set | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/hr_set_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/hr_set/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Czech | CAC | cs | cs_cac | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/cs_cac_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/cs_cac/index.html) |  |
|  | FicTree | cs | cs_fictree | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/cs_fictree_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/cs_fictree/index.html) |  |
|  | PDT | cs | cs_pdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/cs_pdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/cs_pdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Danish | DDT | da | da_ddt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/da_ddt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/da_ddt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Dutch | Alpino | nl | nl_alpino | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/nl_alpino_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/nl_alpino/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | LassySmall | nl | nl_lassysmall | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/nl_lassysmall_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/nl_lassysmall/index.html) |  |
| English | EWT | en | en_ewt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/en_ewt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/en_ewt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | GUM | en | en_gum | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/en_gum_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/en_gum/index.html) |  |
|  | LinES | en | en_lines | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/en_lines_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/en_lines/index.html) |  |
| Estonian | EDT | et | et_edt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/et_edt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/et_edt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Finnish | FTB | fi | fi_ftb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fi_ftb_models.zip) | 0.2.0 | <a rel="license" href="https://www.gnu.org/licenses/lgpl-3.0.en.html"><img alt="GNU License" style="height:15px; width:auto" src="https://www.gnu.org/graphics/lgplv3-88x31.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fi_ftb/index.html) |  |
|  | TDT | fi | fi_tdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fi_tdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fi_tdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| French | GSD | fr | fr_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fr_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fr_gsd/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | Sequoia | fr | fr_sequoia | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fr_sequoia_models.zip) | 0.2.0 | <a rel="license" href="http://infolingu.univ-mlv.fr/DonneesLinguistiques/Lexiques-Grammaires/lgpllr.html">LGPLLR</a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fr_sequoia/index.html) |  |
|  | Spoken | fr | fr_spoken | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fr_spoken_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fr_spoken/index.html) |  <i class="fas fa-flag" style="color:#fdae61"></i> |
| Galician | CTG | gl | gl_ctg | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/gl_ctg_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/gl_ctg/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | TreeGal | gl | gl_treegal | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/gl_treegal_models.zip) | 0.2.0 | <a rel="license" href="http://infolingu.univ-mlv.fr/DonneesLinguistiques/Lexiques-Grammaires/lgpllr.html">LGPLLR</a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/gl_treegal/index.html) |  <i class="fas fa-flag" style="color:#fdae61"></i> |
| German | GSD | de | de_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/de_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/de_gsd/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Gothic | PROIEL | got | got_proiel | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/got_proiel_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/got_proiel/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Greek | GDT | el | el_gdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/el_gdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/el_gdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Hebrew | HTB | he | he_htb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/he_htb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/he_htb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Hindi | HDTB | hi | hi_hdtb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/hi_hdtb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/hi_hdtb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Hungarian | Szeged | hu | hu_szeged | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/hu_szeged_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/hu_szeged/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Indonesian | GSD | id | id_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/id_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/id_gsd/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Irish | IDT | ga | ga_idt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ga_idt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ga_idt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Italian | ISDT | it | it_isdt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/it_isdt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/it_isdt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
|  | PoSTWITA | it | it_postwita | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/it_postwita_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/it_postwita/index.html) |  |
| Japanese | GSD | ja | ja_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ja_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ja_gsd/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Kazakh | KTB | kk | kk_ktb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/kk_ktb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/kk_ktb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-exclamation-triangle" style="color:#e31a1c"></i> |
| Korean | GSD | ko | ko_gsd | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ko_gsd_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ko_gsd/index.html) |  |
|  | Kaist | ko | ko_kaist | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ko_kaist_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ko_kaist/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Kurmanji | MG | kmr | kmr_mg | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/kmr_mg_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/kmr_mg/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-exclamation-triangle" style="color:#e31a1c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Latin | ITTB | la | la_ittb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/la_ittb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/la_ittb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | Perseus | la | la_perseus | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/la_perseus_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/2.5/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/2.5/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/la_perseus/index.html) |  |
|  | PROIEL | la | la_proiel | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/la_proiel_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/la_proiel/index.html) |  |
| Latvian | LVTB | lv | lv_lvtb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/lv_lvtb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/lv_lvtb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| North Sami | Giella | sme | sme_giella | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sme_giella_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sme_giella/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Norwegian | Bokmaal | no_bokmaal | no_bokmaal | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/no_bokmaal_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/no_bokmaal/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | Nynorsk | no_nynorsk | no_nynorsk | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/no_nynorsk_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/no_nynorsk/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | NynorskLIA | no_nynorsk | no_nynorsklia | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/no_nynorsklia_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/no_nynorsklia/index.html) |  |
| Old Church Slavonic | PROIEL | cu | cu_proiel | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/cu_proiel_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/cu_proiel/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Old French | SRCMF | fro | fro_srcmf | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fro_srcmf_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fro_srcmf/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Persian | Seraji | fa | fa_seraji | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/fa_seraji_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/fa_seraji/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Polish | LFG | pl | pl_lfg | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/pl_lfg_models.zip) | 0.2.0 | <a rel="license" href="https://www.gnu.org/licenses/gpl-3.0.en.html"><img alt="GNU License" style="height:15px; width:auto" src="https://www.gnu.org/graphics/gplv3-88x31.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/pl_lfg/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | SZ | pl | pl_sz | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/pl_sz_models.zip) | 0.2.0 | <a rel="license" href="https://www.gnu.org/licenses/gpl-3.0.en.html"><img alt="GNU License" style="height:15px; width:auto" src="https://www.gnu.org/graphics/gplv3-88x31.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/pl_sz/index.html) |  |
| Portuguese | Bosque | pt | pt_bosque | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/pt_bosque_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/pt_bosque/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Romanian | RRT | ro | ro_rrt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ro_rrt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ro_rrt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Russian | SynTagRus | ru | ru_syntagrus | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ru_syntagrus_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ru_syntagrus/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | Taiga | ru | ru_taiga | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ru_taiga_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ru_taiga/index.html) |  <i class="fas fa-flag" style="color:#fdae61"></i> |
| Serbian | SET | sr | sr_set | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sr_set_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sr_set/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Slovak | SNK | sk | sk_snk | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sk_snk_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sk_snk/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Slovenian | SSJ | sl | sl_ssj | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sl_ssj_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sl_ssj/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
|  | SST | sl | sl_sst | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sl_sst_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sl_sst/index.html) |  |
| Spanish | AnCora | es | es_ancora | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/es_ancora_models.zip) | 0.2.0 | <a rel="license" href="https://www.gnu.org/licenses/gpl-3.0.en.html"><img alt="GNU License" style="height:15px; width:auto" src="https://www.gnu.org/graphics/gplv3-88x31.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/es_ancora/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Swedish | LinES | sv | sv_lines | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sv_lines_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sv_lines/index.html) |  |
|  | Talbanken | sv | sv_talbanken | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/sv_talbanken_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/sv_talbanken/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Turkish | IMST | tr | tr_imst | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/tr_imst_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/tr_imst/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Ukrainian | IU | uk | uk_iu | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/uk_iu_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/uk_iu/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Upper Sorbian | UFAL | hsb | hsb_ufal | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/hsb_ufal_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/hsb_ufal/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> <i class="fas fa-exclamation-triangle" style="color:#e31a1c"></i> <i class="fas fa-flag" style="color:#fdae61"></i> |
| Urdu | UDTB | ur | ur_udtb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ur_udtb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ur_udtb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Uyghur | UDT | ug | ug_udt | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/ug_udt_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/ug_udt/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |
| Vietnamese | VTB | vi | vi_vtb | [download](http://nlp.stanford.edu/software/stanfordnlp_models/0.2.0/vi_vtb_models.zip) | 0.2.0 | <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a> | [<i class="fas fa-file-alt"></i>](https://universaldependencies.org/treebanks/vi_vtb/index.html) |  <i class="fas fa-check" style="color:#33a02c"></i> |