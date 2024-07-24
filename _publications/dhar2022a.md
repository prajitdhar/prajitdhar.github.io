---
layout: pub
type: inproceedings
title: "Evaluating Pre-training Objectives for Low-Resource Translation into Morphologically Rich Languages"
location: Marseille, France
month: 6
year: 2022
spage: 4933
epage: 4943
author:
- Prajit Dhar
- Arianna Bisazza
- Gertjan van Noord
booktitle: "Proceedings of the Language Resources and Evaluation Conference (LREC)"
iurl: https://aclanthology.org/2022.lrec-1.527

---

## Abstract

The scarcity of parallel data is a major limitation for Neural Machine Translation (NMT) systems, in particular for translation into morphologically rich languages (MRLs). An important way to overcome the lack of parallel data is to leverage target monolingual data, which is typically more abundant and easier to collect. We evaluate a number of techniques to achieve this, ranging from back-translation to random token masking, on the challenging task of translating English into four typologically diverse MRLs, under low-resource settings. Additionally, we introduce Inflection Pre-Training (or PT-Inflect), a novel pre-training objective whereby the NMT system is pre-trained on the task of re-inflecting lemmatized target sentences before being trained on standard source-to-target language translation. We conduct our evaluation on four typologically diverse target MRLs, and find that PT-Inflect surpasses NMT systems trained only on parallel data. While PT-Inflect is outperformed by back-translation overall, combining the two techniques leads to gains in some of the evaluated language pairs.
