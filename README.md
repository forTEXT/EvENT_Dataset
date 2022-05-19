# Manual Annotations of Narratological Event Types

[![DOI](https://zenodo.org/badge/476644867.svg)](https://zenodo.org/badge/latestdoi/476644867)

## Overview

This repository provides 41,341 manual annotations of events in German prose texts of the 19th and early 20th century.
The annotation guidelines are published [here](https://zenodo.org/record/5078175#.Yka12-hBxhE).
This dataset was created within the EvENT project at the Technical University Darmstadt.
The EvENT project is part of the priority programme [*Computational Literary Studies*](https://dfg-spp-cls.github.io/)
(CLS), funded by the German Research Foundation (DFG).

## Dataset

All annotations are stored in the Annotations_EvENT.json file.
The annotation data is structured by the annotated texts and the annotators.
Each text is annotated by two annotators.
These annotations are the basis for the gold standard annotations.

```python

{
    "Text 1": {
        "Annotator1": [
            {<annotation_object_1>},
            ...,
            {<annotation_object_n>}
        ],
        "Annotator2": [
            {<annotation_object_1>},
            ...,
            {<annotation_object_n>}
        ],
        "gold_standard": [
            {<annotation_object_1>},
            ...,
            {<annotation_object_n>}
        ]
    },
    "Text 2": {
        ...
    }
}
```

Every annotation is represented in this structure:

```python
{
    "annotation": "In einer Gegend des Harzes wohnte ein Ritter",   # the annotated text span
    "tag": "stative_event",                                         # the event type classification
    "properties": {                                                 # additional classifications depending on the event type
        "unpredictable": [
            0
        ],
        "mental": [
            "no"
        ],
        "representation_type": [
            "narrator_speech"
        ]
    },
    "spans": [                                                      # the text spans; discontinuous annotations are represented by multiple pointer items
        [
            62,
            106
        ]
    ]
}
```

## Plain Texts

Additionally, the annotated texts are provided in the Plain_Texts folder.
The text pointers in the annotations refer to these texts.
