# Dutch (Municipal) Text Simplification Corpora


This repository contains data and links to resources related to the task of simplifying Dutch (municipal) texts.

## Why?
According to recent research, 16% of the people between 16 and 65 in Amsterdam have low literacy skills.
This hinders societal participation in tasks such as voting, paying taxes, reissuing documents, or applying for social benefits.
Thus, as part of our [Amsterdam for All](https://www.amsterdamintelligence.com/projects/amsterdam-for-all) project, we have set on a mission to research the use of AI for measuring and improving the readability of municipal communication. We also hope to inspire others to work on text simplification and related technology.

Further information about the problem of measuring and improving the readability of municipal texts,
and how we make use of the datasets in this repository can be found on the [Amsterdam Intelligence website](https://www.amsterdamintelligence.com/posts/automatically-assessing-and-improving-the-readability-of-municipal-communication),
as well as on [Openresearch](https://openresearch.amsterdam/nl/page/89472/improving-readability).

[//]: # (## Folder Structure)

[//]: # ()
[//]: # (* [`complex-simple-sentences`]&#40;./complex-simple-sentences&#41;: contains an evaluation dataset for the task of sentence-level simplification of Dutch municipal texts )

[//]: # (* [`contextualized-lexical-simplification`]&#40;./contextualized-lexical-simplification&#41;: contains information about an evaluation dataset for Contextualized Lexical Simplification)

[//]: # (* [`resources`]&#40;./resources&#41;: contains various links to resources related to the analysis of text complexity and text simplification in the municipal domain, such as lists of complex words, abbreviations, or other existing corpora)


## Automatic Text Simplification

### Dataset by City of Amsterdam

The City of Amsterdam has published a dataset for the task of sentence-level simplification of Dutch municipal texts.
The dataset consists of 1311 sentence pairs automatically aligned from 50 documents manually simplified by communications experts.

The [`complex-simple-sentences`](./complex-simple-sentences) folder contains the dataset,
as well as further details about its creation.

### Dataset and demo by KU Leuven

In 2023, as part of her [MSc AI thesis](https://clin33.uantwerpen.be/abstract/automatic-sentence-level-simplification-for-dutch/), Charlotte Van de Velde and other researchers from KU Leuven shared the following [text simplification resources](https://huggingface.co/collections/BramVanroy/dutch-simplification-650c7f54a853f6b3f8a25979):
- a [dataset](https://huggingface.co/datasets/BramVanroy/chatgpt-dutch-simplification) of 1267 sentences automatically simplified by using gpt-3.5-turbo
- a [base](https://huggingface.co/BramVanroy/ul2-base-dutch-simplification-mai-2023), [small](https://huggingface.co/BramVanroy/ul2-small-dutch-simplification-mai-2023) and [large](https://huggingface.co/BramVanroy/ul2-large-dutch-simplification-mai-2023) versions of a model fine-tuned on the above-mentioned dataset (using the corresponding [UL2 models](https://huggingface.co/yhavinga))
- a [demo](https://huggingface.co/spaces/BramVanroy/mai-simplification-nl-2023-demo) of the base version

## Lexical Simplification

### Contextualized Lexical Simplification Dataset
The [`contextualized-lexical-simplification`](./contextualized-lexical-simplification) folder contains information about an evaluation dataset for Dutch Contextualized Lexical Simplification,
as well as a reference to the corresponding paper proposing LSBertje - a new Dutch model for the task.

### Difficult Words
The City of Amsterdam maintains a [list of complex words](https://www.amsterdam.nl/schrijfwijzer/moeilijke-woorden/) together with simpler alternatives.

### Municipal Abbreviations
A (partial) list of municipal abbreviations from the municipal domain can be found on [github](https://github.com/Amsterdam/afkortingen).

### Inclusive Language
Due to the overlap in underlying technology, we propose taking inclusive language into account when detecting words or phrases that require substitution or providing suitable alternatives.
The City of Amsterdam maintains [a list of inclusive words](https://www.amsterdam.nl/schrijfwijzer/inclusieve-taal-richtlijnen-tips/inclusieve-woordenlijst/)
as well as a full [list of resources related to inclusive language](https://www.amsterdam.nl/schrijfwijzer/inclusieve-taal-richtlijnen-tips/bronnen-inclusieve-taal/).



## Language Level Analysis and Classification

### NT2Lex resources
According to their [own website](https://cental.uclouvain.be/cefrlex/nt2lex/),
"NT2Lex is a lexical database for Dutch as a foreign language (NT2) that includes frequency distributions of words observed in texts graded along the six-level scale of the Common European Framework of Reference for Languages.
It is a receptive graded lexicon, with word frequencies observed in textbook reading activities and simplified readers targeting learners of Dutch."

There are also online tools for the analysis of the complexity of words in a text, as well as frequency distributions of words along the CEFR scale.


### CEFR Annotations by EDIA
As part of a European Language Grid project, EDIA has developed a dataset of 1200 texts (form diverse data source, including municipal texts such as the once that can be found on the [website of the City of Amsterdam](www.amsterdam.nl)).
The texts are labelled with CEFR readability level and are available under a CC-BY-NC license (academic purposes).

The dataset can be requested on the [company's website](https://www.edia.nl/resources/elg/downloads).



## Contributing

Feel free to help out! [Open an issue](https://github.com/Amsterdam-AI-Team/dutch-municipal-text-simplification/issues), submit a [PR](https://github.com/Amsterdam-AI-Team/dutch-municipal-text-simplification/pulls) or [contact us](https://amsterdamintelligence.com/contact/).


## Acknowledgements

This repository was created by [Amsterdam Intelligence](https://amsterdamintelligence.com/) for the City of Amsterdam.

The resources (linked) in this repository were compiled by colleagues at the City of Amsterdam, as well as researchers from the University of Amsterdam, the Vrije Universiteit Amsterdam, as well as external partners and organizations.

We owe a special thank you to the Communications Department of the City of Amsterdam for providing us with valuable resources, and to [Eliza Hobo](https://www.linkedin.com/in/eliza-hobo-259124145), [Daniel Vlantis](https://www.linkedin.com/in/daniel-v-a60905139/) and [Ayoub Abdelouarit](https://www.linkedin.com/in/ayoub-abdelouarit-185171138/) for their dedication.


## License 

This project is licensed under the terms of the European Union Public License 1.2 (EUPL-1.2).
