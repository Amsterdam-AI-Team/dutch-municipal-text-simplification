# Parallel corpus for (the evaluation of) sentence-level simplification in the Dutch municipal domain

[The corpus](./complex-simple-v1-anonymized.csv) consists of 1311 automatically aligned complex-simple sentence pairs.

## Original documents

For the creation of the dataset, we have used ~50 documents provided by the Communications Department of the City of Amsterdam.
The documents have diverse sources and purposes (e.g. reports, citizen letters, newsletters, etc.) and cover a variety of topics (legal, medical, urban planning, etc.).

The documents were reviewed by an expert and contain edits related to simplification,
but also tone of voice, spelling corrections and other improvements.
For the alignment of the sentence, we have used the original and final version of the documents.

## Alignment

The alignment processed consists of 2 steps. For each document, create candidate complex-simple pairs by:
1) aligning paragraphs (based on TF-IDF similarity)
2) aligning sentences within the aligned paragraphs (based on TF-IDF similarity)

#TODO: More details and script to follow

## Post-processeding

After the initial alignment of sentences we:

- filter the candidate pairs where differences are only in capitalization or punctuation
- drop duplicates
- for every complex sentence where there are multiple possible simple versions, create a new entry by merging all simple versions (under the assumption that a complex sentence was simplified by splitting it into 2 or more simple sentences)
- for every complex sentence, preserve the simple version with the lowest Levenshtein edit-distance

#TODO: More details and script to follow

## Anonymization

In order to publish the dataset, the following changes have been performed to the dataset:

We have removed:
- names (including those of people with public functions such as the gemeentesecretaris) -> substituted with [NAME]
- organizations (with the exception of public organization such as Gemeente Amsterdam and GGD, RIVM) -> substituted with [ORGANIZATION]
- addresses (whenever they included an exact street and number) -> substituted with [ADDRESS]
- phone numbers -> substituted with [NUMBER]
- a handful of sentence posing privacy or information security risks, or containing otherwise sensitive information -> replaced by "xxx xxx xxx" for transparency

Finally, the anonymized version of the dataset does not contain further information about the source documents (e.g. their names),
however, a document ID has been added in order to provide context information about sentences stemming from the same document.

## Acknowledgements

This dataset was created by [Amsterdam Intelligence](https://amsterdamintelligence.com/) for the City of Amsterdam.

We owe a special thank you to the Communications Department of the City of Amsterdam for providing us with the original 48 documents.
We also thank [Daniel Vlantis](https://www.linkedin.com/in/daniel-v-a60905139/) for providing feedback during the dataset creation and for extensive experiments with it.


## License 

This data is licensed under the terms of the European Union Public License 1.2 (EUPL-1.2).
