# RA-VG-DDI:Relation-aware virtual node and dynamic substructure gating network for drug-drug interaction prediction

**Authors**: Mingyu Cong, Luming Jiang, Hongjiang MA, Dongjiang Niu, Ruoxuan Ma
and Zhen Li 

**Article Link**: None (the url will be given after the paper is accepted.)

Note that: The relevant figures will be published in this repository after the paper is published. Please wait patiently.

# Requirement
To run the code, you need the following dependencies:
```
PyTorch >= 3.10.0
PyTorch Geometry == 2.0.3`
rdkit == 2020.09.2
```

# Reimplement

The average performace of RA-VG-DDI can be directly calculated by `evaluate.ipynb`.  

If you have configured the environment and want to verify it yourself:  

1. Download the [DrugBank](https://github.com/jcsun-00/DrugBank) and [Twosides](https://github.com/jcsun-00/Twosides) (Note: `Twosides` requires unzipping the `7z` files), and place the folder according to the following requirements:

```
- drugbank_test /
    - DrugBank /
        - cold_start / ...
        - warm_start / ...
        - ddis.csv
        - drug_smiles.csv
        - id_data_dict_dsn_full_connect.pkl
    - transductive_test.py
    - inductive_test.py
    - ...

- twosides_test /
    - Twosides /
        - fold0 / ...
        - fold1 / ...
        - fold2 / ...
        - ddis.csv
        - drug_smiles.csv
        - id_data_dict_dsn_full_connect.pkl
    - test.py
    - ...
```

2. Run the script to complete multiple experiments (Note: You can modify the script's `comment` variable to customize the comments for each experiment):
```
./repeat.sh
```

3. Calculate the average performance of the model through `evaluate.ipynb`