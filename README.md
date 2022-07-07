# MLflow-project-template
MLflow project template

## STEPS -

### STEP 01- Create a repository by using template repository

### STEP 02- Clone the new repository

### STEP 03- Create a conda environment after opening the repository in VSCODE

```bash
conda create --prefix ./env python=3.7 -y
```

```bash
conda activate ./env
```
OR
```bash
source activate ./env
```

### STEP 04- install the requirements
```bash
pip install -r requirements.txt
```

### STEP 05 - Create conda.yaml file -
```bash
conda env export > conda.yaml
```
### Create the environment from the conda.yml file -
```bash
conda env create -f conda.yml
```

### STEP 06- commit and push the changes to the remote repository

## MLFlow commands

```bash
mlflow run . --no-conda
```

### run any specific entry points in MLproject file
```bash
mlflow run . -e get_data --no-conda
```

### run any specific entry points in MLproject file with different config file
```bash
mlflow run . -e get_data -P config=configs/your_config.yaml --no-conda
```

### run mlflow ui
```bash
mlflow ui
```

### how to serve mlflow model
```bash
mlflow models serve -m <path_to_mlflow_model_from_mlruns> -p 1234
```