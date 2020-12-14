# CycIC3

## Run the evaluation script
`evaluate_entangled.py` takes predictions for the Cycic3a and Cycic3b datasets and outputs three accuracy metrics:
1. The accuracy on dataset a
2. The accuracy on dataset b
3. The accuracy on questions in dataset b where the corresponding question in dataset a was answered correctly.
The predictions should be in `.lst` format. That is, they should contain one answer per line, in the same order as the corresponding dataset, like so:
~~~
1
0
0
1
0
~~~
The script also requires the label files and the `linked_questions.csv` file from the dataset. If the prediction files are named `preds_a.lst` and `preds_b.lst`, an example call might look like this:
```
python3 evaluate_entangled.py \
--cycic3a_preds=preds_a.lst \
--cycic3b_preds=preds_b.lst \
--cycic3a_labels=cycic3a_labels.jsonl \
--cycic3b_labels=cycic3b_labels.jsonl
```
