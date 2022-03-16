# nnsvs-polish-support
Files for Polish NNSVS dataset creation

The repo contains HED and .table files required for NNSVS to support training and using Polish.
The phoneme set is based on Fyń's Arpabet which mimics the way the language is written, as well as some additional phonemes to cover lesser appearing sounds in the language.
The estimated amount of audio required for a high quality result is 2-3 hours without silences.

## Information and Directions

The HED file is written by hand and might not work with other tools without proper modifications.

"SzopaTatyJarka PL NN Phoneme set.txt" is a refference for the phonetic system used in the support.
The /dic folder contains a basic table for phonetic training.
The /hed folders contains the HED file.

You can change the hed file in config.yaml, which is found at `/train/config.yaml`.
Nota that while training you have to change "in_dim" in `/train/conf/train/*/model/*.yaml` to following values if using "sztp_polish.hed":

* acoustic: 317
* duration: 313
* timelag: 313

Special thanks to [Causticism](https://github.com/causticism) for helping me with the project.
