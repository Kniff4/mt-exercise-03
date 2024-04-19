# MT Exercise 3: Pytorch RNN Language Models

This repo shows how to train neural language models using [Pytorch example code](https://github.com/pytorch/examples/tree/master/word_language_model). Thanks to Emma van den Bold, the original author of these scripts. 

# CHANGES MADE TO THE SCRIPTS FOR PART 1
We used the Ubuntu terminal to run all the scripts except the install_packages.sh, because the folder "tools" would for some reason be created empty.
We used powershell to run install_packages.sh.
- install_packages.sh: 
  - We changed pip to pip3
  

- download_data.sh: 
  - On line 27 we changed the link to our novel.
  - On lines 23/25/28/32/36/37/41/42/43 we changed the directory name from grimm to frankenstein.
  - Also on line 32 and 36 we changed python to python3

- train.sh:
  - On line 18 we changed python to python3 and we changed the directory name from grimm to frankenstein.

- generate.sh:
  - On line 17 we changed python to python3
  - On line 18 we changed the directory name fromm grimm to frankenstein.



# Requirements

- This only works on a Unix-like system, with bash.
- Python 3 must be installed on your system, i.e. the command `python3` must be available
- Make sure virtualenv is installed on your system. To install, e.g.

    `pip install virtualenv`

# Steps

Clone this repository in the desired place:

    git clone https://github.com/moritz-steiner/mt-exercise-03
    cd mt-exercise-03

Create a new virtualenv that uses Python 3. Please make sure to run this command outside of any virtual Python environment:

    ./scripts/make_virtualenv.sh

**Important**: Then activate the env by executing the `source` command that is output by the shell script above.

Download and install required software:

    ./scripts/install_packages.sh

Download and preprocess data:

    ./scripts/download_data.sh

Train a model:

    ./scripts/train.sh

The training process can be interrupted at any time, and the best checkpoint will always be saved.

Generate (sample) some text from a trained model with:

    ./scripts/generate.sh


