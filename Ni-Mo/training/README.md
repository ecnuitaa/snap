# Using the training data

The training data is provided in json files, which can be read by any standard json parser. Each json file contains one data group (e.g., Ni3Mo_AIMD, Ni4Mo_elastic, Ni_dopedwith_Mo, etc.) used in the training of the SNAP model.

The data is provided as a list of dicts. Each dict contains one structure with data. The format of the json file is as follows:

```json
[
    {   
        "_id": "a string",
        "params": {"Dict of parameters used for DFT calculations, e.g. pseudopotential, energy cutoff, etc."},
        "group": "Ni3Mo",
        "tags": "Md",
        "structure": {"Dict representation of Structure as output by pymatgen"},
        "num_atoms": 108,
        "outputs": {
            "energy": -619.08666252,
            "forces": [],
            "stress": []
        }
    },
    ...
]
```

