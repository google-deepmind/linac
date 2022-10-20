# LINAC: Lossy Implicit Network Activation Coding (Defence)

This repository contains code for reproducing the LINAC transform introduced
in the ICML 2022 paper: ["Hindering Adversarial Attacks with Implicit Neural
 Representations"](https://proceedings.mlr.press/v162/rusu22a.html) by
 Andrei A Rusu, Dan Andrei Calian, Sven Gowal and Raia Hadsel.

## Abstract

We introduce the **Lossy Implicit Network Activation Coding (LINAC)** defence, an input transformation which successfully hinders several common adversarial attacks on CIFAR-10 classifiers for perturbations up to 8/255 in Linf norm and 0.5 in L2 norm. **Implicit neural representations (INRs)** are used to approximately encode pixel colour intensities in 2D images such that classifiers trained on transformed data appear to have robustness to small perturbations without adversarial training or large drops in performance. The seed of the random number generator used to initialise and train INRs turns out to be necessary information for stronger generic attacks, suggesting its role as a private key. We devise a Parametric Bypass Approximation (PBA) attack strategy for key-based defences, which successfully invalidates an existing method in this category. Interestingly, our LINAC defence also hinders some transfer and adaptive attacks, including our novel PBA strategy. Our results emphasise the importance of a broad range of customised attacks despite apparent robustness according to standard evaluations.


## LINAC Colab [![Open In Colab](https://colab.sandbox.google.com/assets/colab-badge.svg)](https://colab.sandbox.google.com/github/deepmind/linac/blob/main/LINAC.ipynb)

We provide installation and usage instructions within the shared notebook.


### Contents:
* We provide example code for computing the LINAC transform and appropriately configuring the defence.
* We share the parameters of the LINAC defended classifier evaluated in our paper.
* We give example JAX code for loading and performing inference with this model.
  * *We invite future works to evaluate its apparent robustness!*
* We plot representations and reconstructions of a couple of CIFAR-10 images.


## Citing this work


If you use this code (or any derived code) in your work,
please cite the accompanying paper:

```
@InProceedings{rusu2022hindering,
  title = {Hindering Adversarial Attacks with Implicit Neural Representations},
  author =       {Rusu, Andrei A and Calian, Dan Andrei and Gowal, Sven and Hadsell, Raia},
  booktitle =   {Proceedings of the 39th International Conference on Machine Learning},
  pages =   {18910--18934},
  year =   {2022},
  editor =   {Chaudhuri, Kamalika and Jegelka, Stefanie and Song, Le and Szepesvari, Csaba and Niu, Gang and Sabato, Sivan},
  volume =   {162},
  series =   {Proceedings of Machine Learning Research},
  month =   {17--23 Jul},
  publisher =    {PMLR},
  pdf =   {https://proceedings.mlr.press/v162/rusu22a/rusu22a.pdf},
  url =   {https://proceedings.mlr.press/v162/rusu22a.html},
  abstract =   {We introduce the Lossy Implicit Network Activation Coding (LINAC) defence, an input transformation which successfully hinders several common adversarial attacks on CIFAR-10 classifiers for perturbations up to 8/255 in Linf norm and 0.5 in L2 norm. Implicit neural representations are used to approximately encode pixel colour intensities in 2D images such that classifiers trained on transformed data appear to have robustness to small perturbations without adversarial training or large drops in performance. The seed of the random number generator used to initialise and train the implicit neural representation turns out to be necessary information for stronger generic attacks, suggesting its role as a private key. We devise a Parametric Bypass Approximation (PBA) attack strategy for key-based defences, which successfully invalidates an existing method in this category. Interestingly, our LINAC defence also hinders some transfer and adaptive attacks, including our novel PBA strategy. Our results emphasise the importance of a broad range of customised attacks despite apparent robustness according to standard evaluations.}
}
```

## License and disclaimer

Copyright 2022 DeepMind Technologies Limited

All software is licensed under the Apache License, Version 2.0 (Apache 2.0);
you may not use this file except in compliance with the Apache 2.0 license.
You may obtain a copy of the Apache 2.0 license at:
https://www.apache.org/licenses/LICENSE-2.0

All other materials are licensed under the Creative Commons Attribution 4.0
International License (CC-BY). You may obtain a copy of the CC-BY license at:
https://creativecommons.org/licenses/by/4.0/legalcode

Unless required by applicable law or agreed to in writing, all software and
materials distributed here under the Apache 2.0 or CC-BY licenses are
distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the licenses for the specific language governing
permissions and limitations under those licenses.

This is not an official Google product.
