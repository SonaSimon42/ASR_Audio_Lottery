# Hacker Role: Audio Lottery - Speech Recognition Made Ultra-Lightweight, Noise-Robust, and Transferable by Ding et al., 2022

## Team Symphony

Dhiraj Sah 22M0771; Poulami Ghosh 22D0363; Sona Elza Simon 22D1591

## Overview of the paper

Authors of the paper: Shaojin Ding, Tianlong Chen, Zhangyang Wang

Lightweight speech recognition models have seen explosive demands owing to a growing amount of speech-interactive features on mobile devices. Since designing such systems from scratch is non-trivial, practitioners typically choose to compress large (pre-trained) speech models. Recently, lottery ticket hypothesis reveals the existence of highly sparse subnetworks that can be trained in isolation without sacrificing the performance of the full models. In this paper, we investigate the tantalizing possibility of using lottery ticket hypothesis to discover lightweight speech recognition models, that are (1) robust to various noise existing in speech; (2) transferable to fit the open-world personalization; and 3) compatible with structured sparsity. We conducted extensive experiments on CTC, RNN-Transducer, and Transformer models, and verified the existence of highly sparse winning tickets that can match the full model performance across those backbones. We obtained winning tickets that have less than 20% of full model weights on all backbones, while the most lightweight one only keeps 4.4% weights. Those winning tickets generalize to structured sparsity with no performance loss, and transfer exceptionally from large source datasets to various target datasets. Perhaps most surprisingly, when the training utterances have high background noises, the winning tickets even substantially outperform the full models, showing the extra bonus of noise robustness by inducing sparsity.

Link: [Audio Lottery: Speech Recognition Made Ultra-Lightweight, Noise-Robust, and Transferable](https://openreview.net/pdf?id=9Nk6AJkVYB)

## Codes explored
* Implementation of LTH on Conformer backbone provided by the authors
* Decaying Pruning: The LTH algorithm does iterative pruning with pruning percentage d contstant throughout the iterations. In this hacker role, we experiment decaying pruning to obtain better winning tickets (or sparse network) of the model. Decayed pruning is done by reducing the pruning percentage  by a factor (prune_factor) at the number of iterations increases.  
* Layerwise Pruning: 


## Reference

```
@inproceedings{ding2021audio,
  title={Audio lottery: Speech recognition made ultra-lightweight, noise-robust, and transferable},
  author={Ding, Shaojin and Chen, Tianlong and Wang, Zhangyang},
  booktitle={International Conference on Learning Representations},
  year={2021}
}
``` 
