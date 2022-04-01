# Manual Annotations of Narratological Event Types

## Overview

This repository provides 41,341 manual annotations of events in German prose texts of the 19th and early 20th century.
The annotation guidelines are published [here](https://zenodo.org/record/5078175#.Yka12-hBxhE).
This dataset was created within the EvENT project at the Technical University Darmstadt.
The EvENT Project is part of the priority programme [*Computational Literary Studies*](https://dfg-spp-cls.github.io/)
(CLS), funded by the German Research Foundation (DFG).

## Dataset

All annotations are stored in the Annotations_EvENT.json file.
The annotation data is structured by the annotated texts and the annotators.
Each text is annotated by two annotators.
These annotations are the basis for the gold standard annotations.

```json

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

```json
{
    "annotation": "den man gewöhnlich nur den blonden Eckbert nannte",  # the annotated text span
    "tag": "process",                                                   # the event type classification
    "properties": {                                                     # additional classifications depending on the event type
        "mental": [
            "no"
        ],
        "persistent": [
            "2"
        ],
        "representation_type": [
            "narrator_speech"
        ],
        "iterative": [
            "yes"
        ],
        "unpredictable": [
            "0"
        ],
        "intentional": [
            "yes"
        ]
    },
    "start_point": 108,                                                 # the start pointer in the annotated text
    "end_point": 157                                                    # the end pointer in the annotated text
}
```

## Plain Texts

Additionally, the annotated texts are provided in the Plain_Texts folder.
The text pointers in the annotations refer to these texts.
