# Authors' Implementation of DeepSpeech Distances proposed in [*High Fidelity Speech Synthesis with Adversarial Networks*](https://arxiv.org/abs/1909.11646)

This repo provides a code for estimation of **DeepSpeech Distances**, new evaluation metrics for neural speech synthesis.

## Setup
```
conda env create -f environment.yml
conda activate DSD-TF1
```

## Usage
Create "Audio/" directory inside the project and insert all audio files with following structure "Audio/{conversion_name}/{auido_type}/*.wav" then run the Jupyter file.

## Major changes for this fork
This fork is to calculate Fréchet DeepSpeech Distance and Kernel DeepSpeech Distance only of a selected data path.
Added environment file to run it locally.
TODO: Jupyter for Google Colab (the old one from the original repo doesn't work anymore as it's for tensorflow 1.x)

### **Notes**
We provide a tensorflow meta graph file for DeepSpeech2 based on the original one available with the [checkpoint](https://nvidia.github.io/OpenSeq2Seq/html/speech-recognition/deepspeech2.html). The provided file differs from the original only in the lack of map-reduce ops defined by horovod library; therefore the resulting model is equivalent to the original.

This is an 'alpha' version of the API; although fully functional it will be heavily updated and simplified soon.

### **References**

[1] Mikołaj Bińkowski, Jeff Donahue, Sander Dieleman, Aidan Clark, Erich Elsen, Norman Casagrande, Luis C. Cobo, Karen Simonyan, [*High Fidelity Speech Synthesis with Adversarial Networks*](https://arxiv.org/abs/1909.11646), ICLR 2020.

[2] Martin Heusel, Hubert Ramsauer, Thomas Unterthiner, Bernhard Nessler, Sepp Hochreiter, [*GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium*](https://arxiv.org/abs/1706.08500), NeurIPS 2017.

[3] Mikołaj Bińkowski, Dougal J. Sutherland, Michael Arbel, Arthur Gretton, [*Demystifying MMD GANs*](https://arxiv.org/abs/1801.01401), ICLR 2018.