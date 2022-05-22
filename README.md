# nnsvs-polish-support
Files for Polish NNSVS dataset creation

The repo contains HED and .table files required for NNSVS to support training and using Polish.
The phoneme set is based on Fyń's Alphasing which mimics the way the language is written, as well as some additional phonemes to cover lesser appearing sounds in the language.
The estimated amount of audio required for a high-quality result is 1-2 hours without silences.

*Model showcase using our Polish NNSVS library [Albert](https://github.com/SzopaTatyJarka/polish-nnsvs-voicebank-albert)*

https://user-images.githubusercontent.com/101723985/160479192-cc5b7aa1-d454-4399-86dd-0ba916725f86.mp4


## Information and Directions

The HED file is written by hand and might not work with other tools without proper modifications.

"SzopaTatyJarka PL NN Phoneme set.txt" is a reference for the phonetic system used in the support.

The `/dic` folder contains a basic table for phonetic training.

The `/hed` folders contain the HED file.

You can change the hed file in config.yaml, which is found at `/train/config.yaml`.
Note that while training you have to change "in_dim" in `/train/conf/train/*/model/*.yaml` to following values if using one of the hed files:

"sztp_polish.hed":

* acoustic: 306
* in_rest_idx: 8
* in_lfx0_idx: 257
* duration: 302
* timelag: 302

"sztp_polish_mdn.hed":

* acoustic: 195
* in_rest_idx: 8
* in_lfx0_idx: 146
* duration: 191
* timelag: 191

*Special thanks to [Causticism](https://github.com/causticism) for helping with the project.*
