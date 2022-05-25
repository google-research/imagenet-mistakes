# ImageNet Mistakes

This repository contains information related to the paper
["When does dough become a bagel? Analyzing the remaining mistakes on
ImageNet"](https://arxiv.org/abs/2205.04596).

## ImageNet-M and updated ImageNet-Multilabel data.

To evaluate on imagenet2012_multilabel and the ImageNet-M subset,
please visit the TensorFlow datasets page for ["imagenet2012_multilabel"](https://www.tensorflow.org/datasets/catalog/imagenet2012_multilabel), which includes instructions for how to prepare the dataset
and access both evaluation splits using version 3.0.0 of the dataset,
which we have released with this paper.

When evaluating on imagenet2012_multilabel, please see the associated
instructions on that page to evaluate multi-label accuracy.  For
the ImageNet-M split, it suffices to just count standard top-1
multi-label accuracy by checking whether the top predicted label is in
the combination of the 'correct_multi_label' and 'unclear_multi_label'
fields.

The example notebook in the notebooks directory contains example code
for evaluating on these splits, including multi-label accuracy and the
ImageNet-M split using pre-computed logits for the ViT-3B and Greedy
Soups models used in the paper.

## Metadata

 - Class Confusions: We include a list of the individual ImageNet classes
 that the ViT-3B confused, as well as their frequency of confusion. The 
 same data is presented in two formats:
   - `class_confusion_wnids.json` - List of tuples with format
    (wnid_1, wnid_2, frequency_of_occurrence)
   - `class_confusion_synsets.json` - List of tuples with format
    (synset_1, synset_2, frequency_of_occurrence). We use only the first
    term of the synset to make the data more human readable.
 
 - Mistake categorizations: We include a mapping from every mistake made by the
ViT3B and Greedy Soups models to mistake category, mistake severity and the
class id of the prediction made.  For severity, we tried to make a fine-grained
assessment between 'minor' and 'borderline' mistakes, but we collapse these
assessments to just 'minor' in our analysis.
   - `vit3b_mistakes.json`: The mistakes mapping for the ViT3B model.
   - `greedy_soups_mistakes.json`: The mistakes for the Greedy Soups model.

## Citation

If you use any artifacts from this repo, kindly include the following citation 
in your work:

```
@article{vasudevan2022does,
  title={When does dough become a bagel? Analyzing the remaining mistakes on ImageNet},
  author={Vasudevan, Vijay and Caine, Benjamin and Gontijo-Lopes, Raphael and Fridovich-Keil, Sara and Roelofs, Rebecca},
  journal={arXiv preprint arXiv:2205.04596},
  year={2022}
}

```

# License

This code repository is licensed under the Apache License, Version 2.0.

## Disclaimer
This is not an officially supported Google product.

