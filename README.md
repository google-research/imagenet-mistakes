# ImageNet Mistakes

This repository contains information related to the paper
["When does dough become a bagel? Analyzing the remaining mistakes on
ImageNet"]().

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

# License

This code repository is licensed under the Apache License, Version 2.0.

## Disclaimer
This is not an officially supported Google product.

