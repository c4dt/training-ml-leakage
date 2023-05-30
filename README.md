# Training ML leakage

This is the repo for the hands-on part of the ML leakage course organized by C4DT in
collaboration with Carmela Troncoso and Bogdan Kulynych from the [SPRING](https://spring.epfl.ch) Lab.
The training comes after a presentation from Carmela Troncoso on leakage in ML
and is split in the following parts:

0. Leading data and baseline measurements

- [Loading](./ml_load_data.ipynb)

1. Measure population-wise privacy leakage

- [Measurements](./1-population-metric.ipynb)
- [Protection](./1-population-metric-diffpriv.ipynb)

2. Measure true privacy leakage

- [Measurements](./2-reference-metric.ipynb)
- [Protection](./2-reference-metric-diffpriv.ipynb)

## Development

Please copy the file [pre-commit](./pre-commit) to the directory [.git/hooks](.git/hooks).
This will remove all the output from the jupyter notebooks and thus make it easier to `git diff` different
commits.