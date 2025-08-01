# Improving Dialogue Management for DarijaGenie through Neural Coherence Modeling
This code is an implementation of the Local Coherence Discriminator (LCD) and the Hierarchical Transformer (HT) described in:

Morad Litime, "Improving Dialogue Management for DarijaGenie through Neural Coherence Modeling", unpublished manuscript, 2025.

This implementation is based on PyTorch 2.7.1+cu126
## Introduction 
Coherence is such an important outcome of
language learning, it reflects the learner’s ability to produce
meaningful text that follows a logical flow. Coherence is even
more essential in dialogues, it ensures mutual understanding in
human conversation. Historically, coherence has been an active
field of research in natural language processing, going from the
early rule-based and linguistic theories to the latest data-driven
neural methods. Our focus is coherence checking for language
learning. Previous work has been done to develop DarijaGenie,
a tool that enables learners to practice the Darija language via
scenario-based interaction with a bot. The primary objective of
this work is to replace the existing dialogue management
framework in DarijaGenie with a new system that leverages a
coherence detection tool. Our general approach is to evaluate
the performance of two architectures on the task of 2-way
classification and integrate the best performer into
DarijaGenie.

## Datasets
You can extract the different Zip files containing the dialogues 

Each Zip file is specific to a training setting:

-"final_datasets" are used for LCD in-domain 

-"final_datasets_cross" and "Test" are used in LCD cross-domain and HT cross-domain

-"final_datsets_train" and "final_datasets_test" are used for HT in-domain

## Training process
In case you wanted to run training from scratch you can go ahead and run the cells in the provided notebooks

Each model has two notebooks each for a training setting (in-domain and cross-domain)

## Using trained models

In case you wanted to use the trained models you can download the following ".pt" files (you can choose the ones you want to test) and follow the instructions.

-"best_lcd_in.pt": For the most performing version of our trained LCD in in-domain settings : https://drive.google.com/file/d/1n_Mj2eISebf1cGJ8q1gybkLu6GkVL6l8/view?usp=drive_link

-"best_lcd_cross.pt": For the most performing version of our trained LCD in cross-domain settings : https://drive.google.com/file/d/17GHZB3vZh8aaYJrLH1fKtKwsO-9NaHQq/view?usp=drive_link

-"best_HT_in.pt": For the most performing version of our trained HT in in-domain settings : https://drive.google.com/file/d/1uWE1iMY4nu9jp4ePnZPlwNYNn8oBieC7/view?usp=drive_link

-"best_HT_cross.pt": For the most performing version of our trained HT in cross-domain settings :  https://drive.google.com/file/d/1FveDTsuA3SIOwu1cTKNd91i0sWcxLTXD/view?usp=drive_link

Make sure you have all the necessary files in a folder.

Here is an example: 

```python
your_folder/
├── final_datasets/   # or any other needed dataset specified in the "Datasets" section depending on what you want to test
.
.
.
├── best_lcd_in.pt   # or any other needed .pt file depending on what you want to test
.
.
.
└── LCD_in_final.ipynb   # or any other needed notebook depending on what you want to test
```

After setting up the folder you can run all the cells in the chosen notebook except the cell starting with comment ```# Training cell (Skip if using pre-trained model)```

## License

This dataset is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).  

Please cite our work as the following if you use this data in your research:

```python
@misc{MORLI-DCORPORA,
  author = {Morad Litime},
  title = {Darija Dialogues Corpora},
  year = {2025},
  url = {https://github.com/iIMoRaD31/Darija-Coherence-assessment-},
  note = {CC BY 4.0}
}

```

## Citations

@article{gaanoun2023darijabert,
  title={Darijabert: a Step Forward in Nlp for the Written Moroccan Dialect},
  author={Gaanoun, Kamel and Naira, Abdou Mohamed and Allak, Anass and Benelallam, Imade},
  year={2023}
}

