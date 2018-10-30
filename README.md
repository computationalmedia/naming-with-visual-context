# Choosing Names with Visual Context

This repository stores supporting data for the WACV'15 [paper](https://ieeexplore.ieee.org/document/7045939):
>Mathews, A., Xie, L. and He, X., 2015, January. Choosing Basic-Level Concept Names Using Visual and Language Context. In Applications of Computer Vision (WACV), 2015 IEEE Winter Conference on (pp. 595-602). IEEE.

and the ACMMM'15 MMCommons Workshop [paper](https://dl.acm.org/citation.cfm?doid=2814815.2814817):

> Mathews, A., Xie, L. and He, X., 2015, October. Studying Object Naming with Online Photos and Caption. In Proceedings of the 2015 Workshop on Community-Organized Multimodal Mining: Opportunities for Novel Solutions (pp. 31-36). ACM.

## Choosing Basic-Level Concept Names

### Abstract

We study basic-level categories for describing visual concepts, and empirically observed context-dependant basic-level names across thousands of concepts. We propose methods for predicting basic-level names using a series of classification and ranking tasks, producing the first large-scale catalogue of basic-level names for hundreds of thousands of images depicting thousands of visual concepts. We also demonstrate the usefulness of our method with a picture-to-word task, showing strong improvement (0.17 precision at slightly higher recall) over recent work by Ordonez et al, and observing significant effects of incorporating both visual and language context for classification. Moreover, our study suggests that a model for naming visual concepts is an important part of any automatic image/video captioning and visual story-telling system.

### Description of Files

We have released a catalogue ([csv](/basic_level_catalogue.csv), [pickle](/basic_level_catalogue.pik)) of the 783 synsets where visual context was found to aid in naming. These synsets correspond to those in Figure 3 marked as showing notable improvement. Note that entries in the catalogue have an index; a smaller index indicates that naming of the synset was improved more by visual context.

We have also released our training datasets and our testing dataset (SBU-148K), which are derived from the [SBU dataset](http://vision.cs.stonybrook.edu/~vicente/sbucaptions/). Our release consists of flickr ids, matching those in the SBU dataset, paired with the filtered list of nouns extracted from the image caption. The dataset is available [here](/word_prediction_benchmark.zip) as an archive containing pickle files. Full accuracy results for each synset are published [here](/synset_accuracy_bnv_v_freqdesc.csv).

For comparison purposes a full set of results is available [here](/comparison_dataset.7z). This dataset also includes: the most frequent noun for each synset, synset detections for the testing set and the results used to generate Figure 3 (in [the paper](/basic_level.pdf)).

## Studying Object Naming with Online Photos and Caption

### Abstract
We explore what names people use to describe visual concepts and why these names are chosen. Choosing object names has been a topic of interest in cognitive psychology, but a systematic, data-driven approach for naming at the scale of thousands of objects does not yet exist. First, we find that visual context has interpretable effects on visual naming, by analysing the MSCOCO dataset that has manually
annotated objects and captions containing the natural language names for the object. We show that taking into account
other objects as context helps improve the prediction of object names. We then analyse the naming patterns on a
large dataset from Flickr, using automatically detected concepts. Preliminary results indicate that naming patterns can
be identified on a large scale, but contrary to the conventional wisdom in cognitive psychology, are not dominated
by genus for animals. We further validate the automatic method with a pilot Amazon Mechanical Turk naming experiment,
and explore the impact of automatic concept detectors with t-SNE visualizations.

### Description of Files

Using the SBU 1-Million image-caption dataset we have calculated the level at which each animal concept is named. The results are provided as heat-maps for the animal classes: mammals, birds and reptiles.

[Mammalia (mammals)](/animal_naming_heatmaps/heat_map_mammals.html)
[Aves (birds)](/animal_naming_heatmaps/heat_map_birds.html)
[Reptilia (reptiles)](/animal_naming_heatmaps/heat_map_reptiles.html)

The level of name used to describe different animals. The first row is the most general level, and the last is the most specific. Each column is a different animal corresponding to a visual classifier. Darker colours indicate larger counts; with columns normalised. Each column must have at least 20 detections to be included. The hover-text shows the names which where matched to the animal and level. Name frequencies are also provided in the hover-text.
