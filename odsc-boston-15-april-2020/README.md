# Accelerate AI/ML Workflows in Hybrid Cloud with Red Hat OpenShift Kubernetes Platform and CognitiveScale Cortex Certifai

https://odsc.com/speakers/accelerate-ai-ml-workflows-in-hybrid-cloud-with-red-hat-openshift-kubernetes-platform-and-cognitivescale-certifai/


# Prerequisites

1) Download the Certifai toolkit - https://www.cognitivescale.com/download-certifai/
2) Python is installed - https://www.python.org/downloads/
3) Conda is installed - https://docs.conda.io/en/latest/miniconda.html
4) Windows users must use PowerShell and have access to the folder where the toolkit was unzipped.

# Install the Certifai Toolkit

1) Set your context to the toolkit folder where you unzipped the contents of the Certifai Toolkit .zip during the download process.

```
cd <path-to-folder-where-toolkit-was-unzipped>
```

2) Create a Python 3.6 virtual environment.

```
conda create -n certifai python=3.6
```

3) Activate the newly created environment.

```
conda activate certifai
```

4) (To enable the use of Jupyter notebooks) Install the base requirements.

```
pip install -r requirements.txt
```

5) Install the CERTIFAI packages

##### For Mac or Linux

```
pip install packages/all/*
pip install packages/python3.6/*
```

##### For Windows PowerShell

```
Get-ChildItem .\packages\all\*.zip | ForEach-Object -Process { pip install $_ }
Get-ChildItem .\packages\python3.6\*.zip | ForEach-Object -Process { pip install $_ }
```

6) Verify that the Certifai CLI and client libraries are installed successfully.

```
certifai -h
```

### Excersise 1

#### What you will learn
* How to launch local Certifai Console
* How Cortex Certifai projects are structured
* Explore use case details
* How the scan was setup
* Evaluate few reports

#### Explore Sample Reports provided with the Certifai Toolkit:

```
cd <path-to-folder-where-toolkit-was-unzipped>
certifai console examples/reports
```
The Console is available at: http://localhost:8000. Copy this URL into a browser to view your scan result visualizations.

#### Follow instructor how to explore Use Case its related models and Certifai Scan


### Excersise 2

#### What you will learn
* We will be demonstrating how to create a scan in Cortex Certifai for your own model.
* Setup an evaluation for fairness, robustness, and explainability.
* Run the scan and explore the evaluation


#### In a terminal or PowerShell window set your context to the Certifai Toolkit notebooks directory


```
cd <path-to-folder-where-toolkit-was-unzipped>
cd examples/notebooks
jupyter notebook
```
We will be using this **tutorials\BringingInYourOwnModel.ipynb** notebook 


#### Follow instructor how to run your own Certifai Scans in Jupyter notebook

