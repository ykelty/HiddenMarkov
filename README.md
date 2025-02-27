This README provides instructions on running the provided code. Follow the steps below to execute the code and generate prediction files.

### Setup Instructions
1. Ensure all required dependency files are present in the same directory:
   - train, dev, test datasets
   - eval.py script
   - CSCI544_HW3.ipynb notebook
2. Update the file paths inside the notebook if needed to match your local setup. Key variables handling file paths include:
   - train, dev, test for datasets
   - output for writing prediction files

### Generating Predictions

#### Running Greedy Decoding
To generate predictions using the greedy decoding algorithm, execute the corresponding code block in the notebook. This will produce:
- `dev_greedy.out` (Predictions on dev set)
- `greedy.out` (Predictions on test set)

#### Running Viterbi Decoding
To generate predictions using the Viterbi algorithm, execute the corresponding code block in the notebook. This will produce:
- `dev_viterbi.out` (Predictions on dev set)
- `viterbi.out` (Predictions on test set)

### Evaluation Instructions
To evaluate the predictions against the gold-standard dataset, use the `eval.py` script outlined for greedy and Viterbi below.
Replace the file names in these commands with your exact file path.
For example, in my code 'dev_greedy.out' is "/content/drive/My Drive/ColabNotebooks/CSCI544_HW3/dev_greedy.out"

#### Evaluating Greedy Decoding Accuracy

!python eval.py -p dev_greedy.out -g dev


#### Evaluating Viterbi Decoding Accuracy

!python eval.py -p dev_viterbi.out -g dev


### File Handling Notes
- All input files are expected to be in the same working directory as the notebook.
- Output files (`*.out`) are stored in the same directory and must match the format of the training data.
- Ensure that the correct dataset (dev or test) is being used when generating predictions.



