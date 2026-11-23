# Validation

The daily input loader and feature/sequence pipeline ran for all five included stocks, each producing 4,947 sequences of shape 60 x 10. TCN, DLinear and LSTM each produced finite two-row predictions. Intraday files were inspected and the default asset list was limited to the supplied EEM file. Full daily/intraday training, hyperparameter sweeps and exact recovery of historical paper metrics were not rerun.

Preparation used Python 3.11 in an existing research environment. These checks are not a clean-environment, end-to-end replication of every result.
