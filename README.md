# Training ML leakage

This is the repo for the hands-on part of the ML leakage course organized by C4DT in
collaboration with Carmela Troncoso and Bogdan Kulynych from the [SPRING](https://spring.epfl.ch) Lab.

## Slides

Here are the slides for the training:

- [Presentation from prof. Carmela Troncoso](./Carmela_Troncoso-ML_Leakage.pdf)
- [Introduction from Linus Gasser](Linus_Gasser-handson_training.pdf)

## Training

The training comes after a presentation from Carmela Troncoso on leakage in ML
and is split in the following parts:

0. Installing all necessary libraries
- [Requirements](./0-requirements.ipynb)

1. Loading data and baseline measurements

- [Loading](./1-ml_load_data.ipynb)

2. Population metric - measure population-wise privacy leakage

- [Measurements](./2.1-population-metric.ipynb)
- [Protection](./2.2-population-metric-diffpriv.ipynb)

3. Reference metric - true privacy leakage

- [Measurements](./3.1-reference-metric.ipynb)
- [Protection](./3.2-reference-metric-diffpriv.ipynb)

## Training slides

You can find the slides from the training here:

[ML leakage metrics](https://docs.google.com/presentation/d/1IU24olmIlSEu5GdmkTRQHd2UMYzXmuLN3F4evNaZOfw/edit)

## Dependencies

It has been tried using python 3.10.9 on a Mac/arm64 and on a docker image.
If you have trouble using it, you can either use a virtual python environment or
try the docker image.

### Python environment

Install it with the following commands on a unix machine:

```bash
python -mvenv venv
. ./venv/bin/activate
pip install jupyter
```

Then you should be able to run the jupyter-notebook like this:

```bash
jupyter-notebook
```

### Docker image of jupyter

You can also use a docker image of the Jupyter Notebook like this:

```bash
docker run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook:python-3.10
```

This should download a suitable docker-image with the jupyter notebook pre-installed.
Open the link indicated once the docker images are downloaded and started.
Then you can open the `work` directory and should see the files.

## Development

Please copy the file [pre-commit](./pre-commit) to the directory [.git/hooks](.git/hooks).
This will remove all the output from the jupyter notebooks and thus make it easier to `git diff` different
commits.

# License

This code is licensed under the MPLv2. 
Its copyright is owned by EPFL.ch.

The original code has been written by [Bogdan Kulynich](https://github.com/bogdan-kulynych) and adopted by
[Linus Gasser](https://github.com/ineiti) in 2023.
