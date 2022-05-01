---
layout: pub
type: inproceedings
title: "Learning to Predict Novel Noun-Noun Compounds"
location: "Florence, Italy"
month: 8
year: 2019
spage: 30
epage: 39
author:
- Prajit Dhar
- Lonneke van der Plas
booktitle: "Proceedings of the Joint Workshop on Multiword Expressions and WordNet (MWE-WN 2019)"
doi: "10.18653/v1/W19-5105"
iurl: https://aclanthology.org/W19-5105

---

## Abstract

We introduce temporally and contextually-aware models for the novel task of predicting unseen but plausible concepts, as conveyed by noun-noun compounds in a time-stamped corpus. We train compositional models on observed compounds, more specifically the composed distributed representations of their constituents across a time-stamped corpus, while giving it corrupted instances (where head or modifier are replaced by a random constituent) as negative evidence. The model captures generalisations over this data and learns what combinations give rise to plausible compounds and which ones do not. After training, we query the model for the plausibility of automatically generated novel combinations and verify whether the classifications are accurate. For our best model, we find that in around 85% of the cases, the novel compounds generated are attested in previously unseen data. An additional estimated 5% are plausible despite not being attested in the recent corpus, based on judgments from independent human raters.
