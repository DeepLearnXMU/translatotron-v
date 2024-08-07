# Translatotron-v

Code for "Translatotron-V(ison): An End-to-End Model for In-Image Machine Translation" (Findings of ACL 2024).


## Install
```
cd src
pip install -e ./
```

## Dataset
Dataset can be downloaded [here](https://drive.google.com/drive/folders/12r54tAQ98Oxtp6Eb3dvaoiOKzu4lD_7h?usp=sharing)

Run `data-build/create_lmdb.sh` to process IIMT data.

## Training

### Stage 1
Run `script/train_mgpu_tiny.sh` to train the image tokenizer.

### Stage 2

1. Run `script/vit-vqgan/run_t2i_layout.sh` to train the teacher model.
2. Run `script/iimt/run_translatotron_v.sh` to train Translatotron-V


## Inference

Run `script/test_translatotron_v.sh` to test Translatotron-V.


## Acknowledgement

- [parti-pytorch
](https://github.com/lucidrains/parti-pytorch): the codebase we built upon. This repository is an implementation of Parti, Google's pure attention-based text-to-image neural network, in Pytorch.
