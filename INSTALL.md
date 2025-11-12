# QDC 2025 Challenge Installation Guide

## Step 0: Create your IBM Cloud account.
[Create an IBM Quantum account](https://quantum.cloud.ibm.com/signin) if you haven't already. **Sign up using the *same email address* you registered with for this event.** Your account will be linked to a specific [instance](https://quantum.cloud.ibm.com/instances) for IBM Quantum services.

## Step 1: Clone repository.

In your terminal, navigate to a folder where you would like to place the QDC 2025 Challenge repository:
```
cd </path/to/your/folder>
```
Then, clone the repository by running:
```
git clone https://github.com/qiskit-community/qdc-challenges-2025.git
```

## Step 2: Create virtual environment.

Please use Python 3.11-3.13. If you do not have one of these versions of Python installed on your machine, please follow the instructions [here](https://www.python.org/downloads/). Then, run the following code in your open terminal:
```
python3 -m venv qdc2025-venv
source qdc2025-venv/bin/activate
```
to create and activate a new virtual environment named **`qdc2025-venv`**.

> **Alternative:** If setting up Python or Jupyter locally is difficult, consider using Google Colab or qBraid. See [this guide](https://quantum.cloud.ibm.com/docs/en/guides/online-lab-environments) for details.


## Step 3: Install required packages.

Finally, install the required packages by running the following line in your open terminal:
```
cd qdc-challenges-2025
pip install -r requirements.txt
```
Note that some challenges use `graphviz` for plotting, which needs to be installed on your machine independently of Python environment. If you do not have `graphviz` on your machine, please follow instructions [here](https://graphviz.org/download/). 

> **If using an online lab environment:** Use the same `requirements.txt` file and pip command to install the required packages. For qBraid, activate the "QDC 2025" environment under the [Environment tab](https://docs.qbraid.com/lab/user-guide/environments), which comes pre-configured. You can launch the  by clicking the button below Launch on qBraid to clone and open this gitHub link on qBraid Lab.

[<img src="https://qbraid-static.s3.amazonaws.com/logos/Launch_on_qBraid_white.png" width="150">](https://account.qbraid.com?gitHubUrl=https://github.com/qiskit-community/qdc-challenges-2025)

## Step 4: Register the virtual environment as a Jupyter kernel.

Run the following lines to register your virtual environment as a Jupyter kernel and launch Jupyter. Once Jupyter launches and you open a challenge notebook, please click **`Kernel > Change Kernel...`** and then select **`QDC 2025`** from the dropdown menu to use the correct virtual environment.
```
python -m ipykernel install --user --name=qdc2025-venv --display-name "QDC 2025"
jupyter notebook
```

## Step 5: Save your token. 

Please navigate to `save_account.ipynb` and run the notebook to save your token. This must be done correctly in order for your challenge submissions to be graded.

You're ready to get started! Good luck :)

___

## DAY 3: Environment for Tutorials

A separate environment is required to run the tutorials located in the `day3_tutorials` folder of this repository. These will be presented on Day 3 of the conference. 

To create a virtual environment for the tutorials, in your terminal navigate to the folder where you cloned the QDC 2025 Challenge repository. Then, repeat Steps 2-4 outlined above, replacing `qdc2025-venv` -> `qdc-tutorials-2025-venv`, `requirements.txt` -> `requirements-tutorials.txt`, and `"QDC 2025"` -> `"QDC Tutorials 2025"` (see the code block below provided for your convenience). In Jupyter, be sure to change the kernel to **`QDC Tutorials 2025`** from the dropdown menu to use the correct virtual environment.
```
cd </path/to/your/folder>
python3 -m venv qdc-tutorials-2025-venv
source qdc-tutorials-2025-venv/bin/activate
cd qdc-challenges-2025
pip install -r requirements-tutorials.txt
python -m ipykernel install --user --name=qdc-tutorials-2025-venv --display-name "QDC Tutorials 2025"
jupyter notebook
```
