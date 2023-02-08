# NNSVS Polish support
Files for Polish NNSVS dataset creation

The repo contains HED and .table files required for NNSVS to support training and using Polish.
The phoneme set is based on Fyń's Alphasing which mimics the way the language is written, as well as some additional phonemes to cover lesser appearing sounds in the language.
The estimated amount of audio required for a high-quality result is 1-2 hours without silences.

*Model showcase using our upcoming Polish NNSVS library Stephan*

https://user-images.githubusercontent.com/101723985/193448118-0c7a374a-e149-43be-b101-22674cc96ff3.mp4

## Information and Directions

The HED file is written by hand and might not work with other tools without proper modifications.

"SzopaTatyJarka PL NN Phoneme set.txt" is a reference for the phonetic system used in the support.

The `/dic` folder contains a basic table for phonetic training.

The `/hed` folders contain the HED file.

You can change the hed file in config.yaml, which is found at `/train/config.yaml`.
Note that while training you have to change "in_dim" in `/train/conf/train/*/model/*.yaml` to values included in the hed files.

*Special thanks to [Intunist team](https://github.com/intunist) for helping with the project.*
