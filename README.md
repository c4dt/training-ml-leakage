# Training ML leakage

This is the repo for the hands-on part of the ML leakage course organized by C4DT in
collaboration with Carmela Troncoso and Bogdan Kulynych.
The training comes after a presentation from Carmela Troncoso on leakage in ML
and is split in the following parts:

1. Measure population-wise privacy leakage
2. Measure true privacy leakage

The jupyter notebooks are the following:

- [Original from Bogdan](./c4dt_privacy.ipynb)
- [Starting to use DiffPrivLib](./c4dt_privacy-secureit.ipynb)
- [Trying to get ml_privacy_meter to work](./c4dt_privacy-meter.ipynb)

## Development

Please copy the file [pre-commit](./pre-commit) to the directory [.git/hooks](.git/hooks).
This will remove all the output from the jupyter notebooks and thus make it easier to `git diff` different
commits.